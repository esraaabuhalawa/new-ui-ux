<template>
    <section class="nav-top">
        <div class="d-lg-block d-none">
            <nav class="navbar-expand-lg" :class="['navbar ', { scrolled: isScrolled }]">
                <div class="container-fluid">
                    <a class="navbar-brand" href="#">
                        <img src="../../assets/images/logo-1.svg" style="width: 60px;">
                    </a>
                    <ul class="navbar-nav" style="gap: 30px;">
                        <li class="nav-item">
                            <a class="nav-link active" aria-current="page" href="#services">Services</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#about">About</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#portofolio">Portofolio</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#Testmonials">Testimonials</a>
                        </li>

                        <li class="nav-item">
                            <button> <a href="tel:+1234567890" class="d-inline-block w-100"> Book Call Now </a></button>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
        <!-----For Small Devices----------->
        <div class="d-lg-none d-flex justify-content-between mx-4 mt-2">
            <div>
                <img src="../../assets/images/logo-1.svg" style="width: 60px;">
            </div>
            <button id="OpenMenu" class="btn" type="button" aria-controls="offcanvasExample">
                <svg class="w-6 h-6 text-gray-800 dark:text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                    width="24" height="24" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-width="2" d="M5 7h14M5 12h14M5 17h14" />
                </svg>
            </button>
        </div>

        <!--Offcanvas Start-->
        <div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvasExample"
            aria-labelledby="offcanvasExampleLabel" ref="offcanvas">
            <div class="offcanvas-header">
                <h5 class="offcanvas-title" id="offcanvasExampleLabel">
                    <img src="../../assets/images/logo-1.svg" style="width: 60px;">
                </h5>
                <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"
                    @click="closeOffcanvas"></button>
            </div>
            <div class="offcanvas-body">
                <ul class="navbar-nav flex-column" style="gap: 30px;">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#services">Services</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#portofolio">Portofolio</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#Testmonials">Testimonials</a>
                    </li>

                    <li class="nav-item position-fixed" style="bottom: 15px;">
                        <button>Book Call Now</button>
                    </li>
                </ul>
            </div>
        </div>
        <!--Offcanvas End-->
    </section>
</template>
<script>
export default {
    data() {
        return {
            isScrolled: false,
        };
    },
    methods: {
        handleScroll() {
            // Update state based on scroll position
            this.isScrolled = window.scrollY > 0;
        },
        closeOffcanvas(event) {
            event.preventDefault(); // Prevent the default behavior
            // Close the offcanvas programmatically
            const offcanvasEl = this.$refs.offcanvas;
            const bsOffcanvas = bootstrap.Offcanvas.getInstance(offcanvasEl);
            if (bsOffcanvas) {
                bsOffcanvas.hide();
            }
        },
        toggleOffcanvas(event) {
            event.preventDefault();
            event.stopPropagation(); // Prevent scrolling to the top
            const offcanvasEl = this.$refs.offcanvas;
            let bsOffcanvas = bootstrap.Offcanvas.getInstance(offcanvasEl);

            if (!bsOffcanvas) {
                // Initialize the Bootstrap Offcanvas instance if not already done
                bsOffcanvas = new bootstrap.Offcanvas(offcanvasEl);
            }

            bsOffcanvas.toggle(); // Toggle the offcanvas
        },
    },
    mounted() {
        // Add scroll event listener when the component is mounted
        window.addEventListener('scroll', this.handleScroll);

        // Setup the event listener for the menu toggle
        const openMenuBtn = document.getElementById("OpenMenu");
        if (openMenuBtn) {
            openMenuBtn.addEventListener("click", this.toggleOffcanvas);
        }
    },
    beforeDestroy() {
        // Remove scroll event listener to prevent memory leaks
        window.removeEventListener('scroll', this.handleScroll);

        // Clean up event listener for the menu button
        const openMenuBtn = document.getElementById("OpenMenu");
        if (openMenuBtn) {
            openMenuBtn.removeEventListener("click", this.toggleOffcanvas);
        }
    },
};
</script>

<style lang="scss" scoped>
.navbar {
    margin-bottom: 30px;
    padding-left: 48px;
    padding-right: 48px;
    padding-top: 12px;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 10000;
}

.navbar.scrolled {
    background: #fff;
    /* Change to desired background color */
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
    /* Optional shadow */
}
</style>