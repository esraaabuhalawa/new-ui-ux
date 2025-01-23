<template>
    <div class="new-achievement-section pt-100 pb-70 my-4">
        <div class="container">
            <div class="row d-flex align-items-center align-content-md-end">
                <section class="col-lg-3 col-md-6 mt-3 mt-lg-0 text-center">
                    <div class="features-content" ref="projectRef">
                        <h4><span>+</span>{{ ourProjects }}</h4>
                        <p>
                            projects
                        </p>
                    </div>
                </section>

                <section class="col-lg-3 col-md-6 mt-3 mt-lg-0 text-center">
                    <div class="features-content" ref="clientsRef">
                        <h4>
                            <span>+</span>{{ clients }}
                        </h4>
                        <p>
                            courses
                        </p>
                    </div>
                </section>

                <section class="col-lg-3 col-md-6 mt-3 mt-lg-0 text-center">
                    <div class="features-content" ref="employeesRef">
                        <h4>
                            <span>+</span>{{ employees }}
                        </h4>
                        <p>
                            clients
                        </p>
                    </div>
                </section>

                <section class="col-lg-3 col-md-6 mt-3 mt-lg-0 text-center">
                    <div class="features-content" ref="ratingRef">
                        <h4>
                            <span>+</span>{{ trainers }}
                        </h4>
                        <p>
                            years of exprience
                        </p>
                    </div>
                </section>
            </div>


            <!---------------->
            <div>
                <header class="section-title">
                    <h3> I Am Available For Your Project </h3>
                    <p>
                        I am here to elevate your digital experiences! With my expertise as a Senior UI/UX Designer, I
                        specialize in crafting user-centric designs, mentoring teams, and consulting on innovative
                        solutions to help your business stand out and connect with your audience on a deeper level."
                    </p>
                    <a  href="tel:+1234567890">get start today</a>
                </header>
            </div>
            <!------------------->
        </div>
    </div>
</template>

<script>
export default {
    name: "Features",
    data() {
        return {
            ourProjects: 0,
            clients: 0,
            employees: 0,
            rating: 0,
            observer: null,
        };
    },
    mounted() {
        this.observer = new IntersectionObserver(this.handleIntersection, {
            root: null,
            rootMargin: "0px",
            threshold: 0.5, // Trigger when half of the element is visible
        });

        this.observer.observe(this.$refs.projectRef);
    },
    methods: {
        handleIntersection(entries) {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    this.startCounting("ourProjects", 120);
                    this.startCounting("clients", 10);
                    this.startCounting("employees", 100);
                    this.startCounting("trainers", 6);
                    this.observer.unobserve(entry.target);
                }
            });
        },
        startCounting(property, value) {
            let current = 0;
            const interval = setInterval(() => {
                current++;
                this[property] = current;
                if (current === value) {
                    clearInterval(interval);
                }
            }, 50); // Adjust speed as needed
        },
    },
};
</script>
<style lang="scss" scoped>
.container {
    padding: 20px 60px;
    margin-top: 60px;
    margin-bottom: 60px;

    .row {
        padding-top: 83px;
        padding-bottom: 83px;
        margin-bottom: 50px;
    }

    section {
        h4 {
            font-size: 50px;
        }

        p {
            font-size: 28px;
            color: #42307D;
            font-weight: 600;
            text-transform: uppercase;
        }
    }
}

.section-title {
    text-align: center;

    h3 {
        font-family: "Birthstone", serif;
        font-size: 50px;
        font-weight: 800;
    }

    p {
        margin-top: 30px;
        font-size: 20px;
        margin-bottom: 40px;
    }

    a {
        display: inline-block;
        padding: 10px 40px;
        background: #42307D;
        color: #fff;
        border-radius: 40px;
        font-size: 20px;
        text-transform: capitalize;
        cursor: pointer;
        text-decoration: none;
        transition: all .5s ease-in-out;

        &:hover {
            transform: translateY(5px);
        }
    }
}

@media screen and (max-width: 992.8px) {
    .col-lg-3{
        margin-bottom: 40px;
    }
}
</style>