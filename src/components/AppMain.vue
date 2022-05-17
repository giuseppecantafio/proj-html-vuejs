<template>
  <div>
    <div class="main-wrapper">
      <div class="main-container">
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
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppMain",
};
</script>

<style scoped lang="scss">
@import "../style/vars.scss";
.main-wrapper {
  padding-top: 150px;
  width: 100%;
  background: linear-gradient(
    0deg,
    rgba(226, 226, 224, 1) 0%,
    rgba(255, 255, 255, 1) 100%
  );
  .main-container {
    width: 80%;
    margin: 0 auto;
    .text-container {
      width: 70%;
      margin: 0 auto;
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
        top: -75px;
        right: 10px;
        z-index: 2;
      }
      .img-container-3 {
        position: absolute;
        bottom: -20px;
        right: 20px;
      }
      .img-container-4 {
        position: absolute;
        top: -50px;
        right: 64px;
      }
      .shape-container-5{
        width: 55px;
        height: 55px;
        position: absolute;
        left: -100px;
        top: 0;
        div{
          width: 55px;
          height: 55px;
          border: 7px solid #ECC5AB;
        }
      }
    }
  }
}
</style>

// position: relative; // &:after { // content: ""; // position: absolute; //
top: 80%; // left: 0; // height: 100px; // width: 100%; // background:
url("../assets/images/svg-1.svg") bottom center; // }
