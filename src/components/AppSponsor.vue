<template>
  <div>
    <div class="main-container">
      <!--INIZIO PRIMO BLOCCO-->
      <div class="container-fluid first-block">
        <div class="row">
          <div class="col-6 col-left">
            <div class="text-container">
              <p class="first">testimonials</p>
              <div class="h1">
                <strong>Why Do People </strong><span>&ast;Hearts&ast;</span>
                <strong> Us?</strong>
              </div>
              <p class="second py-2 text-justify">
                Seeking for verbals of our service quality? Find them here.
                everything is trasparent and straightforward for your sense of
                justification.
              </p>
              <p class="third">
                <strong>
                  <a href="#"
                    >View all <i class="fa-solid fa-arrow-right"></i
                  ></a>
                </strong>
              </p>
            </div>
          </div>
          <div class="col-6 col-right d-flex align-items-center">
            <div
              class="testimonial-box hvr-grow hvr-underline-from-left"
              @mouseover="stopSlider"
              @mouseleave="startSlider"
            >
              <div class="my-testimonial">
                <h2 class="uppertext">
                  {{ myTestimonials[indice].upperText }}
                </h2>
                <p class="middletext">
                  {{ myTestimonials[indice].middleText }}
                </p>
                <div class="testimonial-info container-fluid">
                  <div class="row align-items-center">
                    <div class="col-2">
                      <div class="img-container">
                        <img
                          :src="
                            require('../assets/images/' +
                              myTestimonials[indice].img)
                          "
                          :alt="myTestimonials[indice].name"
                          class="img-fluid rounded-circle"
                        />
                      </div>
                    </div>
                    <div class="col-10">
                      <div class="name">{{ myTestimonials[indice].name }}</div>
                      <div class="job">{{ myTestimonials[indice].job }}</div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!--/FINE PRIMO BLOCCO-->
      <!--INIZIO SECONDO BLOCCO-->
      <div class="container-fluid second-block">
        <div class="row">
          <div class="col-6 col-left">
            <div class="mother-container">
              <div class="img-container-1">
                <img
                  src="../assets/images/home-3-team-image.png"
                  class="img-fluid"
                  alt="Group"
                />
              </div>
              <div class="img-container-2">
                <img
                  src="../assets/images/maxcoach-shape-05-150x150.png"
                  alt="shape"
                />
              </div>
              <div class="img-container-3">
                <img
                  src="../assets/images/maxcoach-shape-07-150x150.png"
                  alt="shape"
                />
              </div>
              <div class="img-container-4"></div>
              <div class="img-container-5">
                <img src="../assets/images/maxcoach-shape-01.png" alt="shape" />
              </div>
              <div class="shape-container-6">
                <div class="rounded-circle"></div>
              </div>
            </div>
          </div>
          <div
            class="col-6 col-right d-flex justify-content-center align-items-center"
          >
            <div class="text-container">
              <p class="first">Everything in <strong>MaxCoach</strong></p>
              <div class="h1">
                <strong>We're Here To </strong><span>Transform</span>
                <strong> You</strong>
              </div>
              <p class="second py-2 text-justify">
                As learners, people can enjoy great companionship from MaxCoach
                mentors and educators. We can help you develop and grow at your
                best.
              </p>
              <p class="third">
                <strong>
                  <a
                    href="#"
                    class="myButton rounded mt-3 mx-5 hvr-grow text-center"
                    ><span
                      >Get Free Guide
                      <i class="fa-solid fa-arrow-right"></i></span
                  ></a>
                </strong>
              </p>
            </div>
          </div>
        </div>
      </div>
      <!--/FINE SECONDO BLOCCO-->
    </div>
    <!--INIZIO TERZO BLOCCO-->
    <div class="third-block">
      <div class="blog-container">
        <div class="blog-intro text-center">
          <p>Read for more joyment</p>
          <div class="h1">
            <strong>Latest from </strong><span>Our Blogs</span>
          </div>
        </div>
        <div class="container-fluid">
          <div class="row">
            <div
              class="col-4 text-center cards-container"
              v-for="(post, index) in myPosts"
              :key="index"
            >
              <app-blog :item="post" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--/FINE TERZO BLOCCO-->
    <!--INIZIO QUARTO BLOCCO-->
    <div class="newsletter-wrapper text-center">
      <div class="nl-intro">
        <div class="h1"><strong>Subscribe </strong><span>Newsletter</span></div>
        <p>
          Enter your email address to register to our newsletter subscription
          delivered on a regular basis
        </p>
      </div>
      <div class="nl-bar hvr-grow">
        <div class="input-group mb-3">
          <input
            type="text"
            class="form-control"
            placeholder="Enter your email"
            aria-label="Enter your email"
            aria-describedby="basic-addon2"
          />
          <div class="input-group-append">
            <button class="btn" type="button">Subscribe</button>
          </div>
        </div>
      </div>
      <div class="img-container-1">
        <img src="../assets/images/maxcoach-shape-02.png" alt="shape" />
      </div>
      <div class="img-container-2">
        <img src="../assets/images/maxcoach-shape-09.png" alt="shape" />
      </div>
      <div class="shape-container-3">
        <div class="rounded-circle"></div>
      </div>
    </div>
  </div>
</template>

<script>
import dati from "../dati.json";
import AppBlog from "./AppBlog.vue";

export default {
  components: { AppBlog },
  name: "AppSponsor",
  data() {
    return {
      myTestimonials: dati.testimonials,
      myPosts: dati.posts,
      indice: 0,
      intervallo: null,
    };
  },
  methods: {
    startSlider() {
      this.intervallo = setInterval(() => {
        if (this.indice === 3) {
          this.indice = 0;
        } else {
          this.indice += 1;
        }
      }, 3000);
    },
    stopSlider() {
      clearInterval(this.intervallo);
      this.intervallo = null;
    },
  },
  mounted() {
    this.startSlider();
  },
};
</script>

<style scoped lang="scss">
@import "../style/vars.scss";
//MAIN AND GENERAL RULES
.main-container {
  padding-top: 80px;
  width: 70%;
  margin: 0 auto;
  //PRIMO BLOCCO
  .first-block {
    .col-left {
      .text-container {
        width: 70%;
        .first {
          text-transform: uppercase;
        }
        .first,
        .second,
        .third {
          color: $storm-dust;
        }
        .h1 span {
          color: $mountain-meadow;
        }
        a {
          color: $dark;
        }
      }
    }
    .col-right {
      .testimonial-box {
        cursor: default;
        .my-testimonial {
          padding: 25px;
          .uppertext {
            font-size: 1.4rem;
          }
          .middletext {
            text-align: justify;
            font-weight: 600;
            color: $storm-dust;
            padding: 10px 0px;
            font-size: 0.7rem;
          }
          .testimonial-info {
            padding-left: 0;
          }
          .img-container {
            width: 60px;
            height: 60px;
          }
          .name {
            text-transform: uppercase;
            font-size: 0.8rem;
            font-weight: 700;
          }
          .job {
            font-size: 0.7rem;
            color: $delta;
          }
        }
      }
    }
  }
  //SECONDO BLOCCO
  .second-block {
    padding-top: 80px;
    .col-right {
      .text-container {
        width: 70%;
        .first {
          text-transform: uppercase;
        }
        .first,
        .second,
        .third {
          color: $storm-dust;
        }
        .h1 span {
          color: $mountain-meadow;
        }
        .myButton {
          width: 250px;
          padding: 10px 5px;
          background-color: $mountain-meadow;
          color: $white;
        }
      }
    }
    .col-left {
      .mother-container {
        height: 500px;
        position: relative;
        .img-container-1 {
          position: absolute;
          top: 0;
          z-index: 6;
        }
        .img-container-2 {
          position: absolute;
          top: 100px;
          left: -100px;
          z-index: 5;
        }
        .img-container-3 {
          position: absolute;
          bottom: -50px;
          right: 130px;
          z-index: 4;
        }
        .img-container-4 {
          height: 152px;
          width: 150px;
          background-image: url("../assets/images/svg-2.svg");
          background-size: 150px 152px;
          filter: opacity(50%);
          position: absolute;
          top: 0;
          left: -20px;
          z-index: 3;
        }
        .img-container-5 {
          position: absolute;
          bottom: 0px;
          left: -200px;
        }
        .shape-container-6 {
          width: 55px;
          height: 55px;
          position: absolute;
          top: -50px;
          right: -70px;
          div {
            width: 55px;
            height: 55px;
            border: 7px solid #ecc5ab;
          }
        }
      }
    }
  }
}
//TERZO BLOCCO
.third-block {
  margin-top: 90px;
  background-color: rgba(226, 226, 224, 1);
  .blog-container {
    width: 70%;
    margin: 0 auto;
    .blog-intro {
      p {
        padding-top: 70px;
        text-transform: uppercase;
        color: $storm-dust;
      }
      .h1 span {
        color: $mountain-meadow;
      }
    }
  }
  .cards-container {
    padding-top: 50px;
    padding-bottom: 50px;
  }
}
//QUARTO BLOCCO
.newsletter-wrapper {
  padding-top: 40px;
  padding-bottom: 40px;
  height: 300px;
  width: 30%;
  margin: 0 auto;
  position: relative;
  .nl-intro {
    .h1 span {
      color: $mountain-meadow;
    }
    p {
      padding-top: 10px;
      color: $storm-dust;
      font-size: 0.8rem;
      font-weight: 600;
    }
  }
  .nl-bar {
    width: 400px;
    .input-group {
      .btn {
        border-top-left-radius: 0;
        border-bottom-left-radius: 0;
        border-top-right-radius: 0.2rem;
        border-bottom-right-radius: 0.25rem;
        border: 1px solid $mountain-meadow;
        background-color: $mountain-meadow;
        color: $light;
      }
      .form-control {
        border: 1px solid rgba(226, 226, 224, 1);
        background-color: rgba(226, 226, 224, 1);
      }
    }
  }
  .img-container-1 {
    position: absolute;
    top: 100px;
    right: -300px;
  }
  .img-container-2 {
    position: absolute;
    top: 20px;
    right: -300px;
  }
  .shape-container-3 {
    width: 55px;
    height: 55px;
    position: absolute;
    left: -300px;
    bottom: 40px;
    filter: opacity(40%);
    div {
      width: 55px;
      height: 55px;
      border: 7px solid $mountain-meadow;
    }
  }
}
</style>
