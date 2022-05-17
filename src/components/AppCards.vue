<template>
  <div>
    <a href="#" class="hvr-float-shadow">
      <div class="card" style="width: 18rem">
        <img
          class="card-img-top"
          :src="require('../assets/images/' + item.img)"
          :alt="item.text"
        />
        <div class="card-body">
          <h5 class="card-title"><span>&dollar;</span>{{ item.price }}</h5>
          <p class="card-text">
            {{ item.text }}
          </p>
          <div class="d-flex justify-content-start card-info">
            <p><i class="fa-solid fa-paste px-1"></i>{{ item.lessons }}</p>
            <p><i class="fa-solid fa-user px-1"></i>{{ item.students }}</p>
          </div>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: "AppCards",
  props: {
    item: Object,
  },
};
</script>

<style lang="scss">
@import "../style/vars.scss";
a {
  text-align: left !important;
  .card-title {
    color: $mountain-meadow;
  }
  .card-text {
    color: $dark;
    font-weight: 600;
    &:hover {
      color: $mountain-meadow;
    }
  }
  .card-info {
    color: $storm-dust;
    font-size: 0.8rem;
    p {
      padding: 5px;
    }
  }
}
</style>
