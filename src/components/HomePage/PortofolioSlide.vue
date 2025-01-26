<template>
  <div>
    <div class="container pb-70 clients">
      <div class="section__heading justify-content-between row">
        <div class="col-lg-7">
          <h2>Lets have a look at my <span>Portfolio</span></h2>
        </div>
        <div class="col-lg-2 offset-lg-3">
          <a href="https://www.behance.net/nourhanmahmoud7" target="blank">
            see all
          </a>
        </div>
      </div>
    </div>

    <div class="container-fluid our-clients overflow-hidden">
      <Carousel v-bind="settings" :breakpoints="breakpoints" :autoplay="2000" :wrap-around="true">
        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/181767661/UX-case-study-Medical-website" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-4.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">UMEDMI</h5>
                <p class="card-text text-dark">App - Web design</p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/200681071/Case-Study-Buy-2-(-Employee-Management-)" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-2.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">BUY2</h5>
                <p class="card-text text-dark">App </p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/212078273/ITAMEN-AI-Doctor-AI-Diagnosis" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">ITAMEN -AI Diagnosis</h5>
                <p class="card-text text-dark">Web Design</p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/181767661/UX-case-study-Medical-website" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-4.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">UMEDMI</h5>
                <p class="card-text text-dark">App - Web design</p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/200854539/Sari3-web-design-_-partner-dashboard" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-6.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">Dashboard</h5>
                <p class="card-text text-dark">App - Web design</p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a class="card text-decoration-none" href="https://www.behance.net/gallery/193331345/Payment-HUB-web-design" target="blank">
              <img src="../../assets/images/project-7.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">Payment</h5>
                <p class="card-text text-dark">App HUB</p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/186771099/PLAYIT-App-design-Chat-Enhancement" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-8.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">Play IT</h5>
                <p class="card-text text-dark">App </p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>

        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/200681071/Case-Study-Buy-2-(-Employee-Management-)" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-2.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">BUY2</h5>
                <p class="card-text text-dark">App </p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>


        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/212109485/ITAMEN-App-AI-doctors" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-10.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">ITAMEN -AI Diagnosis</h5>
                <p class="card-text text-dark">web Design</p>
              </div>
            </a>
            <!--------------->
          </div>
        </Slide>


        <Slide>
          <div class="carousel__item">
            <!--------------->
            <a href="https://www.behance.net/gallery/212269191/Domino-Game" target="blank" class="card text-decoration-none">
              <img src="../../assets/images/project-11.png" class="card-img-top" alt="..." />
              <div class="card-body">
                <h5 class="card-title">Domino Game</h5>
                <p class="card-text text-dark">web Design</p>
              </div>
            </a>
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
          itemsToShow: 2,
          snapAlign: "center",
        },
        900: {
          itemsToShow: 3,
          snapAlign: "center",
        },
        // 1024 and up
        1024: {
          itemsToShow: 4,
          snapAlign: "center",
        },
      } /*********/,
    };
  },
});
</script>
<style lang="scss" scoped>
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

.section__heading {
  padding-top: 70px;
  padding-bottom: 50px;

  a {
    display: inline-block;
    padding: 10px 40px;
    background: #42307d;
    color: #fff;
    border: 2px solid #42307d;
    border-radius: 40px;
    font-size: 20px;
    text-transform: capitalize;
    cursor: pointer;
    text-decoration: none;
    transition: all 0.5s ease-in-out;

    &:hover {
      transform: translateY(5px);
      color: #42307d;
      background: transparent;
    }
  }
}

.card {
  background-color: #7f56d90a;
  padding: 10px;
  padding-bottom: 20px;
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
}

.card-body {
  img {
    border: 2px solid #fff;
    border-top-left-radius: 20px;
    border-top-right-radius: 20px;
  }

  font-family: "Poppins",
  sans-serif;
  text-align: start;

  .card-title {
    color: #42307d;
    font-size: 24px;
    font-weight: 500;
    text-transform: uppercase;
  }

  .card-text {
    font-size: 20px;
    font-weight: 500;
    text-transform: uppercase;
  }
}
</style>