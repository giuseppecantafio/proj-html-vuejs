<template>
  <div>
    <header class="debug">
      <nav>
        <div class="container debug">
          <div class="row d-flex justify-content-center debug">
            <div class="col-5 debug">
              <ul class="d-flex justify-content-between">
                <li v-for="(item, index) in myDati"
                  :key="index"
                >
                  {{ item.name }}
                </li>
              </ul>
            </div>
            <div class="col-3 debug">
              <img
                :src="require('../assets/images/dark-logo.png')"
                alt="Logo"
              />
            </div>
            <div class="col-4 debug">a</div>
          </div>
        </div>
      </nav>
      <div class="jumbotron"></div>
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
nav {
  height: 80px;
  width: 100%;
  .container {
    height: 100%;
    width: 100%;
    .row {
      height: 100%;
      div {
        height: 100%;
      }
    }
  }
}
</style>
