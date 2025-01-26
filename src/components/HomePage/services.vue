<template>
    <section id="services" ref="servicesSection"  class="">
        <div class="section__heading text-center">
            <h2 class="text-capitalize" :class="{ typewriter: isInView }">My <span>services</span></h2>
        </div>
        <div class="services-bg">
            <div class="container">
                <section class="row">
                    <div class="col-lg-4 col-md-6  mb-3 mb-lg-0">
                        <!------first card----->
                        <div class="d-flex gap-3 position-relative">
                            <div class="service-card">
                                <h3>Apps</h3>
                                <div class="service-card-bg-1">
                                    <div class="service-card-bg">
                                        <div class="service-card-bg-2">
                                            <img src="../../assets/images/service-1.png" alt="service" class="img-fluid">
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="service-arrow">
                                <div class="service-arrow-1">
                                    <img src="../../assets/images/up right.png">
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-4 col-md-6  mb-3 mb-lg-0">
                        <!------first card----->
                        <div class="d-flex gap-3 position-relative">
                            <div class="service-card ">
                                <h3>web design</h3>
                                <div class="service-card-bg-1">
                                    <div class="service-card-bg">
                                        <div class="service-card-bg-2">
                                            <img src="../../assets/images/service-2.png" alt="service" class="img-fluid">
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="service-arrow">
                                <div class="service-arrow-1">
                                    <img src="../../assets/images/up right.png">
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-4 col-md-6  mb-3 mb-lg-0">
                        <!------first card----->
                        <div class="d-flex gap-3 position-relative">
                            <div class="service-card ">
                                <h3>dashboard</h3>
                                <div class="service-card-bg-1">
                                    <div class="service-card-bg">
                                        <div class="service-card-bg-2">
                                            <img src="../../assets/images/service-3.png" alt="service" class="img-fluid">
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="service-arrow">
                                <div class="service-arrow-1">
                                    <img src="../../assets/images/up right.png">
                                </div>
                            </div>
                        </div>
                    </div>
                </section>

            </div>
        </div>

    </section>
</template>
<script>
export default {
  data() {
    return {
      isInView: false, // Tracks whether the section is in view
    };
  },
  mounted() {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            this.isInView = true; // Trigger the animation
            observer.unobserve(this.$refs.servicesSection); // Stop observing after animation starts
          }
        });
      },
      { threshold: 0.5 } // Adjust this value for when the animation starts
    );

    observer.observe(this.$refs.servicesSection);
  },
}
</script>
<style lang="scss" scoped>
    .col-lg-4{
        display: flex; 
        justify-content: center;
    }
</style>