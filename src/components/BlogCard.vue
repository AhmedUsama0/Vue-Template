<template>
  <div class="blog-card" :style="{ backgroundColor: background }">
    <div class="blog-pad">
      <h3>{{ header }}</h3>
      <div class="span-container">
        <span>{{ name }}</span>
        <span>{{ category }}</span>
      </div>
    </div>

    <img :src="require(`@/assets/Blog/${img}`)" alt="" />
  </div>
</template>

<script>
export default {
  name: "BlogCard",
  props: ["background", "img", "header", "name", "category", "className"],
};
</script>

<style lang="scss" scoped>
.blog-card {
  //   border: 2px solid;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  .blog-pad {
    padding: 30px;

    h3 {
      text-align: left;
      color: #000;
      font-size: 29px;
      font-weight: normal;
    }

    .span-container {
      //   border: 2px solid;
      margin-top: 35%;
      span {
        display: block;
        text-align: left;
        text-transform: capitalize;
        font-size: 13px;
        color: #000;

        // border:2px solid;

        &:nth-child(2) {
          margin-top: 10px;
          margin-bottom: 20px;
          text-transform: uppercase;
          font-size: 11px;
          letter-spacing: 1px;
          //   border: 2px solid;
        }
      }
    }
  }

  img {
    // border: 2px solid;
    vertical-align: bottom;
    width: 100%;
    height: auto;
  }
}


@media screen and(max-width:700px) {
    .blog-card{
        grid-column-start: 1;
        grid-column-end: 4;
    }
}

@media screen and(min-width:701px) and(max-width:929px) {
  .blog-card{
    .blog-pad {
      h3{
        font-size: 15px;
      }
    }
  }
}
</style>
