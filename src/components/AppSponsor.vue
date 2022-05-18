<template>
  <div>
    <div class="main-container">
      <!--INIZIO PRIMO BLOCCO-->
      <div class="container-fluid">
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
            <div class="testimonial-box hvr-grow hvr-underline-from-left" @mouseover="stopSlider" @mouseleave="startSlider">
              <div
                class="my-testimonial"
              >
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
    </div>
  </div>
</template>

<script>
import dati from "../dati.json";

export default {
  name: "AppSponsor",
  data() {
    return {
      myTestimonials: dati.testimonials,
      indice: 0,
      intervallo: null
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

<style lang="scss">
@import "../style/vars.scss";
//MAIN AND GENERAL RULES
.main-container {
  padding-top: 80px;
  width: 70%;
  margin: 0 auto;
  //PRIMO BLOCCO
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
</style>
