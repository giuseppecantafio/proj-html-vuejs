<template>
  <div>
    <div class="main-wrapper">
      <div class="main-container">
        <!--INIZIO PRIMO BLOCCO-->
        <div class="first-block">
          <div class="container-fluid">
            <div class="row">
              <div class="col-6 col-left">
                <div class="text-container">
                  <p class="first">everything in <strong>maxcoach</strong></p>
                  <div class="h1">
                    <strong>Learn about our </strong><span>Work Culture</span>
                    <strong> at MaxCoach</strong>
                  </div>
                  <p class="second py-2 text-justify">
                    Spend some time to visit our website of head office and
                    discover our current courses, enrollment procedure, and
                    registration deadline. We're opening new classes every
                    beginning each month.
                  </p>
                  <p class="third">
                    Have questions?
                    <strong>
                      <a href="#"
                        >Get Free Guide <i class="fa-solid fa-arrow-right"></i
                      ></a>
                    </strong>
                  </p>
                </div>
              </div>
              <div
                class="col-6 col-right d-flex justify-content-center align-items-center"
              >
                <div class="img-container-1">
                  <img
                    src="../assets/images/stock-full-hd-10-ohki1ayywq3cqutettrncduujpoaorifqu4relt2ts.jpg"
                    class="img-fluid rounded"
                    alt="People in a room"
                  />
                </div>
                <div class="img-container-2">
                  <img
                    src="../assets/images/about-us-01-ohkia3qg98rq9vg3s0mn2hkflr1migdqdw370qnegc.jpg"
                    alt="Woman"
                    class="img-fluid rounded"
                  />
                </div>
                <div class="img-container-3">
                  <img
                    src="../assets/images/maxcoach-shape-02.png"
                    alt="element"
                  />
                </div>
                <div class="img-container-4">
                  <img
                    src="../assets/images/maxcoach-shape-07.png"
                    alt="element"
                  />
                </div>
                <div class="shape-container-5">
                  <div class="rounded-circle"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!--/FINE PRIMO BLOCCO-->
        <!--INIZIO SECONDO BLOCCO-->
        <div class="second-block">
          <div class="container-fluid">
            <div class="row">
              <div class="col-4 col-left">
                <h2>129&plus;</h2>
                <p>enroalled learners</p>
              </div>
              <div class="col-4 col-center">
                <h2>80</h2>
                <p>finished sessions</p>
              </div>
              <div class="col-4 col-right">
                <h2>4&percnt;</h2>
                <p>satisfaction rate</p>
              </div>
            </div>
          </div>
        </div>
        <!--/FINE SECONDO BLOCCO-->
        <!--INIZIO TERZO BLOCCO-->
        <div class="third-block">
          <div class="container-fluid">
            <div class="row">
              <div class="col-8 col-left">
                <div class="img-container-1">
                  <img
                    src="../assets/images/stock-full-hd-11-670x450.jpg"
                    alt="woman"
                    class="img-fluid rounded"
                  />
                </div>
                <div class="yt-player-container">
                  <a href="#">
                    <img
                      src="../assets/images/icon-youtube-play.png"
                      alt="youtube play"
                    />
                  </a>
                </div>
                <div class="img-container-2"></div>
                <div class="img-container-3">
                  <img
                    src="../assets/images/maxcoach-shape-05-150x150.png"
                    alt="shape"
                  />
                </div>
                <div class="img-container-4">
                  <img
                    src="../assets/images/maxcoach-shape-07-150x150.png"
                    alt="shape"
                  />
                </div>
                <div class="shape-container-5">
                  <div class="rounded-circle"></div>
                </div>
              </div>
              <div class="col-4 col-right">
                <div class="text-container">
                  <p class="first">how we work</p>
                  <div class="h1">
                    <strong>Upgrade your skill </strong
                    ><span>Upgrade your life</span>
                  </div>
                  <p class="second py-2 text-justify">
                    Opening up more opportunities in front of you to get the
                    ticket to more enjoyable door in life. Getting equipped with
                    new skills for new sets of insights into your caree.
                    MaxCoach accompany learners in every stage of learning.
                  </p>
                  <p class="third">
                    <strong>
                      <a href="#"
                        >Download free guidebook
                        <i class="fa-solid fa-arrow-right"></i
                      ></a>
                    </strong>
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!--/FINE TERZO BLOCCO-->
        <!--INIZIO QUARTO BLOCCO-->
        <div class="fourth-block">
          <div class="cards-intro text-center">
            <p>Join MaxCoach at best</p>
            <div class="h1">
              <strong>Latest Online </strong><span>Courses</span>
            </div>
          </div>
          <div class="container-fluid">
            <div class="row">
              <div
                class="col-4 text-center cards-container"
                v-for="(card, index) in myCards"
                :key="index"
              >
                <app-cards :item="card" />
              </div>
            </div>
          </div>
        </div>
        <!--/FINE QUARTO BLOCCO-->
      </div>
    </div>
  </div>
</template>

<script>
import dati from "../dati.json";
import AppCards from "./AppCards.vue";

export default {
  name: "AppMain",
  components: {
    AppCards,
  },
  data() {
    return {
      myCards: dati.cards,
    };
  },
};
</script>

<style scoped lang="scss">
@import "../style/vars.scss";
//MAIN AND GENERAL RULES FOR APPMAIN
.main-wrapper {
  padding-top: 150px;
  width: 100%;
  background: linear-gradient(
    0deg,
    rgba(226, 226, 224, 1) 0%,
    rgba(255, 255, 255, 1) 100%
  );
  position: relative;

  &:after {
    content: "";
    position: absolute;
    top: 95%;
    left: 0;
    height: 100px;
    width: 100%;
    background: url("../assets/images/svg-1.svg") bottom center;
  }
  .main-container {
    width: 70%;
    margin: 0 auto;
    //PRIMO BLOCCO
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
      .h1 span,
      a {
        color: $mountain-meadow;
      }
    }
    .col-right {
      position: relative;

      .img-container-1 {
        width: 480px;
        height: 300px;
        z-index: 1;
      }
      .img-container-2 {
        width: 150px;
        height: 150px;
        position: absolute;
        top: -65px;
        right: 10px;
        z-index: 2;
      }
      .img-container-3 {
        position: absolute;
        bottom: -20px;
        right: 0px;
      }
      .img-container-4 {
        position: absolute;
        top: -50px;
        right: 64px;
      }
      .shape-container-5 {
        width: 55px;
        height: 55px;
        position: absolute;
        left: -100px;
        top: 0;
        div {
          width: 55px;
          height: 55px;
          border: 7px solid #ecc5ab;
        }
      }
    }
    //SECONDO BLOCCO
    .second-block {
      padding-top: 50px;
      width: 60%;
      margin: 0 auto;
      text-align: center;
      h2 {
        color: $mountain-meadow;
        font-weight: 700;
      }
      p {
        text-transform: uppercase;
        font-size: 1rem;
        color: $storm-dust;
        font-weight: 600;
      }
    }
    //TERZO BLOCCO
    .third-block {
      padding-top: 100px;

      .col-left {
        position: relative;

        .img-container-1 {
          height: auto;
          width: auto;
          position: absolute;
          top: 0;
          z-index: 6;
        }
        .yt-player-container {
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
          z-index: 7;
        }
        .img-container-2 {
          height: 152px;
          width: 150px;
          background-image: url("../assets/images/svg-0.svg");
          background-size: 150px 152px;
          position: absolute;
          top: -50px;
          left: -50px;
          z-index: 3;
        }
        .img-container-3 {
          position: absolute;
          top: 50px;
          left: -80px;
          z-index: 4;
        }
        .img-container-4 {
          position: absolute;
          bottom: -85px;
          right: 10px;
          z-index: 2;
        }
        .shape-container-5 {
          width: 55px;
          height: 55px;
          position: absolute;
          right: -100px;
          top: -80px;
          z-index: 1;
          div {
            width: 55px;
            height: 55px;
            border: 7px solid #ecc5ab;
          }
        }
      }
      .col-right {
        .text-container {
          width: 100%;
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
    }
    // QUARTO BLOCCO
    .fourth-block {
      padding-top: 150px;

      .cards-intro {
        p {
          text-transform: uppercase;
          color: $storm-dust;
        }
        .h1 span {
          color: $mountain-meadow;
        }
      }
      .cards-container {
        padding-top: 50px;
        padding-bottom: 100px;
      }
    }
  }
}
</style>
