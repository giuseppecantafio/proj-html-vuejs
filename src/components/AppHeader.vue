<template>
  <div>
    <header>
      <!--INIZIO NAV-->
      <nav>
        <div class="container">
          <div class="row d-flex justify-content-center align-items-center">
            <div class="col-5 col-left">
              <ul class="d-flex justify-content-start align-items-center">
                <li v-for="(item, index) in myDati" :key="index" class="px-2">
                  <a :href="item.link"
                    >{{ item.name }} <i class="fa-solid fa-angle-down"></i
                  ></a>
                </li>
              </ul>
            </div>
            <div class="col-3 col-center">
              <div class="img-container d-flex align-items-center">
                <img
                  :src="require('../assets/images/dark-logo.png')"
                  alt="Logo"
                  class="img-fluid"
                />
              </div>
            </div>
            <div class="col-4 col-right d-flex align-items-center">
              <div class="d-flex align-items-center">
                <div
                  class="shopping-container flex-container d-flex align-items-center"
                >
                  <i class="fa-solid fa-cart-shopping"></i>
                  <div class="shopping-counter">0</div>
                </div>
                <i class="fa-solid fa-circle-user px-2"></i>
                <div class="flex-container d-flex align-items-center">
                  <i class="fa-solid fa-magnifying-glass"></i>
                  <input
                    class="form-control"
                    type="search"
                    placeholder="Search"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </nav>
      <!--/FINE NAV-->
      <!--INIZIO JUMBOTRON-->
        <div class="jumbotron d-flex justify-content-center align-items-center">
          <div class="info-container text-center">
            <h2>Commence Business</h2>
            <h1>Distant Mentoring Program</h1>
            <div class="myButton">Download free guidebook <i class="fa-solid fa-arrow-right"></i></div>
          </div>
        </div>
      <!--/FINE JUMBOTRON-->
    </header>
  </div>
</template>

<script>
import dati from "../dati.json";
export default {
  name: "AppHeader",
  data() {
    return {
      myDati: dati.header,
    };
  },
};
</script>

<style scoped lang="scss">
@import "../style/vars.scss";

// NAVBAR
nav {
  height: 80px;
  width: 100%;
  .container {
    height: 100%;
    width: 100%;
    .row {
      height: 100%;
      .col-left,
      .col-center,
      .col-right {
        height: 100%;
        ul {
          height: 100%;
          a {
            color: $dark;
          }
        }
        .img-container {
          height: 100%;
          width: 50%;
        }
        .shopping-container {
          position: relative;
          .shopping-counter {
            font-size: 0.6rem;
            font-weight: 700;
            height: 15px;
            width: 15px;
            line-height: 15px;
            vertical-align: middle;
            text-align: center;
            color: $light;
            background-color: $mountain-meadow;
            border-radius: 50%;
            position: absolute;
            top: -10px;
            right: -8px;
          }
        }
        .flex-container {
          position: relative;
          input {
            background-color: $search-bg;
            border: none;
          }
          .fa-magnifying-glass {
            color: $mountain-meadow;
            position: absolute;
            right: 5px;
          }
        }
      }
    }
  }
}

//JUMBOTRON
.jumbotron{
  height: 600px;
  width: 100%;
  background-image: url('../assets/images/home-3-hero-bg.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  .info-container{
    color: $light;
  }
}
</style>
