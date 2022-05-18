<template>
  <div>
    <div class="footer-container">
      <div class="footer-wrapper">
        <div class="container-fluid">
          <div class="row">
            <div class="col-6 col-left">
              <h2>Address</h2>
              <div
                class="elements py-2"
                v-for="(address, index) in myAddress"
                :key="index"
              >
                {{ address.name }}
              </div>
              <div
                class="social-contacts d-flex justify-content-start align-items-center"
              >
                <a
                  href="#"
                  class="py-3"
                  v-for="(icon, index) in myIcons"
                  :key="index"
                >
                  <i :class="icon.icon" class="hvr-pop"></i>
                </a>
              </div>
            </div>
            <div class="col-6 col-right">
              <div class="container-fluid">
                <div class="row">
                  <div class="col-4">
                    <h2>Explore</h2>
                    <div
                      class="elements py-2"
                      v-for="(explore, index) in myExplore"
                      :key="index"
                    >
                      {{ explore.name }}
                    </div>
                  </div>
                  <div class="col-4 extra">
                    <div
                      class="elements py-2"
                      v-for="(extra, index) in myExtra"
                      :key="index"
                    >
                      {{ extra.title }}
                    </div>
                  </div>
                  <div class="col-4">
                    <h2>Information</h2>
                    <div
                      class="elements py-2"
                      v-for="(information, index) in myInformation"
                      :key="index"
                    >
                      {{ information.name }}
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="credits text-center">
            &copy; 2020 Maxcoach. All Rights Reserved
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import dati from "../dati.json";

export default {
  components: {},
  name: "AppFooter",
  data() {
    return {
      myAddress: dati.address,
      myIcons: dati.icons,
      myExplore: dati.explore,
      myExtra: dati.extraexplore,
      myInformation: dati.information,
    };
  },
};
</script>

<style scoped lang="scss">
@import "../style/vars.scss";

.footer-container {
    padding-top: 50px;
  width: 100%;
  height: 350px;
  background-color: $vulcan;
  .footer-wrapper {
    width: 70%;
    margin: 0 auto;
  }
  .col-left {
    h2 {
        font-size: 1.5rem;
      color: $white;
    }
    .elements {
      color: $delta;
      cursor: pointer;
      &:hover {
        color: $white;
        transition: color 1s ease-in-out;
      }
    }
    .social-contacts {
      a {
        color: $delta;
        padding-right: 20px;
        i {
          font-size: 1.5rem;
          &:hover {
            color: $white;
            transition: color 1s ease-in-out;
          }
        }
      }
    }
  }
  .col-right {
    h2 {
        font-size: 1.5rem;
      color: $white;
    }
    .elements {
      color: $delta;
      cursor: pointer;
      &:hover {
        color: $white;
        transition: color 1s ease-in-out;
      }
    }
    .extra {
      margin-top: 48px;
    }
  }
  .credits{
      padding-top: 25px;
      color: $delta;
  }
}
</style>
