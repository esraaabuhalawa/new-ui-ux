<template>
  <div id="Testmonials">
    <div class="container pt-35 pb-70 clients">
      <div class="section__heading text-center">
        <h2>Testimonials That Speak to <span>My Results</span></h2>
      </div>
    </div>
    <div class="container-fluid our-clients overflow-hidden">
      <Carousel
        v-bind="settings"
        :breakpoints="breakpoints"
        :autoplay="2000"
        :wrap-around="true"
      >
        <Slide>
          <div class="carousel__item">
            <!--------------->
            <div class="card">
              <div class="card-body">
                <img src="../../assets/images/quote-down.png" />
                <p class="card-text">
                  "Nourhan’s designs have significantly improved our user
                  engagement. Her creative ideas and problem-solving skills
                  brought our platform to life. Highly recommended!"
                </p>
                <h5 class="card-title">Tarek Ahmed </h5>
              </div>
            </div>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <div class="card">
              <div class="card-body">
                <img src="../../assets/images/quote-down.png" />
                <p class="card-text">
                  "By God, you make my face shine, Miss Nourhan. Thank you for your work and effort. Your work is very, very wonderful."
                </p>
                <h5 class="card-title">Tarek Ahmed </h5>
              </div>
            </div>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <div class="card">
              <div class="card-body">
                <img src="../../assets/images/quote-down.png" />
                <p class="card-text">
                  "Nourhan's work on our mobile app was revolutionary. Their innovative touch transformed our app into a seamless, engaging, and responsive experience that users now rave about. They truly understand the nuances of mobile UX."
                </p>
                <h5 class="card-title">Tarek Ahmed </h5>
              </div>
            </div>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <div class="card">
              <div class="card-body">
                <img src="../../assets/images/quote-down.png" />
                <p class="card-text">
                  "Nourhan has a rare talent for turning complex ideas into seamless, user-friendly designs. Their ability to anticipate user needs and deliver intuitive by interfaces helped our product stand out in a competitive market. Their work consistently exceeds expectations."
                </p>
                <h5 class="card-title">Tarek Ahmed </h5>
              </div>
            </div>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <div class="card">
              <div class="card-body">
                <img src="../../assets/images/quote-down.png" />
                <p class="card-text">
                  "Working with Nourhan is a game-changer for any development team. Their designs are not only visually appealing but also technically feasible and well-documented, making the implementation process smooth and efficient. Their collaborative approach fosters synergy between design and development."
                </p>
                <h5 class="card-title">Tarek Ahmed </h5>
              </div>
            </div>
            <!--------------->
          </div>
        </Slide>

      </Carousel>
    </div>
  </div>
</template>
  <script>
import { defineComponent } from "vue";
import { Carousel, Navigation, Slide, Pagination } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";
export default defineComponent({
  name: "OurClients",
  components: {
    Pagination,
    Carousel,
    Slide,
    Navigation,
  },
  data() {
    return {
      settings: {
        itemsToShow: 1,
        snapAlign: "center",
      },
      // breakpoints are mobile first
      // any settings not specified will fallback to the carousel settings
      breakpoints: {
        // 700px and up
        700: {
          itemsToShow: 1,
          snapAlign: "center",
        },
        900: {
          itemsToShow: 1.8,
          snapAlign: "center",
        },
        // 1024 and up
        1024: {
          itemsToShow: 1.8,
          snapAlign: "center",
        },
      } /*********/,
    };
  },
});
</script>
<style lang="scss" scoped>
:root {
  --carousel-transition: 300ms;
  --carousel-opacity-inactive: 0.7;
  --carousel-opacity-active: 1;
  --carousel-opacity-near: 0.9;
}

.carousel__viewport {
  perspective: 2000px;
}

.carousel__track {
  transform-style: preserve-3d;
}

.carousel__slide--sliding {
  transition: opacity var(--carousel-transition),
    transform var(--carousel-transition);
}

.carousel.is-dragging .carousel__slide {
  transition: opacity var(--carousel-transition),
    transform var(--carousel-transition);
}

.carousel__slide {
  opacity: var(--carousel-opacity-inactive);
  transform: translateX(10px) rotateY(-12deg) scale(0.8);
}

.carousel__slide--prev {
  opacity: var(--carousel-opacity-near);
  transform: rotateY(-10deg) scale(0.95);
}

.carousel__slide--active {
  opacity: var(--carousel-opacity-active);
  transform: rotateY(0) scale(1.05);
}

.carousel__slide--next {
  opacity: var(--carousel-opacity-near);
  transform: rotateY(10deg) scale(0.95);
}

.carousel__slide--next ~ .carousel__slide {
  opacity: var(--carousel-opacity-inactive);
  transform: translateX(-10px) rotateY(12deg) scale(0.9);
}

#Testmonials {
  background-image: url("../../assets/images/frame-77.png");
  background-size: cover;
  background-position: center;
  padding: 40px 0;
  padding-bottom: 130px;
  margin-top: 80px;
}

h2 {
  color: #fff;
  font-size: 44px;
  line-height: 1.4;
  width: 500px;
  margin: auto;
  span {
    color: #d2beff;
  }
}

.card {
  background: transparent !important;
}
.card-body {
  background: rgba(255, 255, 255, 0.15);
  border-radius: 15px;
  color: #000;
  position: relative;
  padding: 40px;
  text-align: left;
  .card-title {
    color: #F9FAFB;
    margin-top: 40px;
  }
  .card-text {
    color: #fff;
    line-height: 2;
    height: 110px;
  }
}

.card-body img {
  margin-right: 10px;
  position: absolute;
  top: 20px;
  right: 10px;
  z-index: 1000;
  width: 130px;
  height: auto;
}

.carousel__viewport {
  perspective: 2000px;
}
.carousel__slide {
  position: relative;
}
.carousel__pagination {
  margin-top: 10px;
}
.client-navigation {
  position: absolute;
}
.carousel__slide {
  border-radius: 5px;
  margin-right: 5px;
  padding-top: 10px;
  padding-bottom: 10px;
}

@media screen and (max-width:992px) {
  .card-body {
    .card-text{height: auto;}
  }
}
</style>