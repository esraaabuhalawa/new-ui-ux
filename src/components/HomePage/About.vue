<template>
  <section id="about">
    <div class="section__heading">
      <h2>A little <span>about</span> Me</h2>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-lg-7">
          <div>
            <h3>UX UI designer</h3>
            <p>
              Senior UI UX designer with 6+ years experience in building
              websites, apps and responsive using all updated UX process ideate,
              research , wireframe, test, design and implementation .My
              objectives are to achieve goals & get results for the
              organization/company that i work with as well as personal
              objectives.
            </p>
          </div>
          <div class="mt-40">
            <h3>Ux UI instructor</h3>
            <p>
              Provided comprehensive training and mentorship as a UX/UI design
              instructor, equipping students with industry-standard tools,
              methodologies, and best practices to create user-centered designs
              and impactful digital experiences."
            </p>
          </div>
        </div>

        <div class="col-lg-5 d-flex justify-content-center align-items-center">
          <div>
            <div class="outer-circle">
              <div class="middle-circle">
                <div class="inner-circle">
                  <div class="img-container">
                    <img
                      src="../../assets/images/about-img.png"
                      alt="Person"
                      width="328"
                      height="310"
                    />
                    <div class="play-btn" data-bs-toggle="modal" data-bs-target="#exampleModal">
                      <img src="../../assets/images/Decline.svg" />
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div
      class="modal fade"
      id="exampleModal"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
      ref="modal"
    >
      <div
        class="modal-dialog modal-dialog-centered"
        @click="handleOutsideClick"
      >
        <div class="modal-content">
          <div class="modal-header">
            <button type="button" data-bs-dismiss="modal" aria-label="Close"> 
              <svg
                class="w-6 h-6 text-gray-800 dark:text-white"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  stroke="#fff"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18 17.94 6M18 18 6.06 6"
                />
              </svg>
            </button>
          </div>
          <div class="modal-body" @click.stop>
            <video ref="video" class="w-100" controls>
              <source
                src="../../assets/images/home/1321208-uhd_3840_2160_30fps.mp4"
                type="video/mp4"
              />
              Your browser does not support the video tag.
            </video>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  methods: {
    handleOutsideClick(event) {
      // Check if the click was outside the video
      if (this.video && !this.video.contains(event.target)) {
        this.video.pause();
        this.video.currentTime = 0; // Optionally reset the video
      }
    },
  },
  mounted() {
    // Assign refs after mounting
    this.video = this.$refs.video;
    this.modal = this.$refs.modal;

    // Add Bootstrap modal event listener
    if (this.modal) {
      this.modal.addEventListener("hidden.bs.modal", () => {
        if (this.video) {
          this.video.pause();
          this.video.currentTime = 0; // Optionally reset the video
        }
      });
    }
  },
  beforeDestroy() {
    // Clean up event listener
    if (this.modal) {
      this.modal.removeEventListener(
        "hidden.bs.modal",
        this.handleOutsideClick
      );
    }
  },
};
</script>
<style lang="scss" scoped>
@media screen and (max-width: 992.3px) {
  .col-lg-7 {
    margin-bottom: 100px;
  }
}

.modal-dialog {
  max-width: 60%;
}

.modal-content {
  background: #fff;
  border: 0;
}

.modal-header {
  border-bottom: 0;
  padding: 0px 15px;
  padding-top: 20px;

  button {
    background: #09445d;
    padding: 4px;
    border-radius: 5px;
  }
}

</style>