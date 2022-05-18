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
          <h5 class="card-title">{{ item.section }}</h5>
          <p class="card-text">
            {{ item.text }}
          </p>
          <div class="d-flex justify-content-start card-info">
            <p><i class="fa-solid fa-paste px-1"></i>{{ item.date }}</p>
            <p><i class="fa-solid fa-user px-1"></i>{{ item.views }}</p>
          </div>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: "AppBlog",
  props: {
    item: Object,
  },
};
</script>

<style scoped lang="scss">
@import "../style/vars.scss";
a {
  text-align: left;
  .card {
    border: none;
    background-color: transparent;
    .card-img-top {
      border-bottom-left-radius: calc(0.25rem - 1px);
      border-bottom-right-radius: calc(0.25rem - 1px);
    }
    .card-body {
      padding-left: 0;

      .card-title {
        color: $storm-dust;
        text-transform: uppercase;
        font-size: 0.8rem;
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
          padding-right: 8px;
        }
      }
    }
  }
}
</style>
