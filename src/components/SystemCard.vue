<template>
  <div class="system-card">
    <img
      class="top-image"
      :src="require(`@/assets/Shop/${topImg}`)"
      :alt="topAlt"
    />
    <div class="sys-pad">
      <span>{{ spanHead }}</span>
      <h3>{{ title }}</h3>
      <p>
        {{ pargraph }}
      </p>
      <button>learn more</button>
    </div>
    <img
      class="bottom-image"
      :src="require(`@/assets/Shop/${bottomImg}`)"
      :alt="bottomAlt"
    />
  </div>
</template>

<script>
export default {
  name: "SystemCard",
  props: [
    "spanHead",
    "title",
    "pargraph",
    "bottomImg",
    "bottomAlt",
    "topAlt",
    "topImg",
  ],
};
</script>

<style lang="scss" scoped>
.system-card {
  background-color: #e9e9e9;
  text-align: left;
  border-radius: 5px;
  width: 31%;
  height: 800px;
  overflow: hidden;
  position: relative;

  .top-image {
    float: right;
    max-width: 145px;
    min-height: 200px;
  }
  .sys-pad {
    padding: 30px;
    span {
      font-size: 15px;
      border-bottom: 3px solid #74ddda;
      padding-bottom: 10px;
      text-transform: uppercase;
    }

    h3 {
      margin: 50px 0 20px 0;
      font-size: 30px;
    }

    p {
      margin: 10px 0px;
      max-width: 70%;
      line-height: 25px;
    }

    button {
      display: block;
      background-color: #000;
      margin: 40px 0px;
      color: #fff;
      padding: 15px 25px;
      border: none;
      font-size: 18px;
      cursor: pointer;
      text-transform: capitalize;
    }
  }

  .bottom-image {
    width: 100%;
    position: absolute;
    bottom: 0;
    height: 222px;
  }
}

@media screen and (max-width: 1024px) {
  .system-card {
    width: 100%;
    margin-bottom: 5%;
    .sys-pad {
      h3 {
        font-size: 22px;
      }

      p {
        line-height: 30px;
      }
    }
  }
}

@media screen and (max-width: 330px) {
  .top-image {
    max-width: 135px !important;
  }
}
</style>
