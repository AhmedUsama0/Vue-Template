<template>
  <div class="shop-section">
    <AppHeader background="#FFF"/>
    <div class="shop">
      <div class="container">
        <h1>Shop</h1>
        <ul>
          <li><a href="">Shop all</a></li>
          <li><a href="">Brand Strategy Tools</a></li>
          <li><a href=""> Inspiration Tools</a></li>
          <li><a href=""> Contnet Strategy Tools</a></li>
          <li><a href="">Systems</a></li>
          <li><a href="">WorkShops</a></li>
          <li><a href="">Programs</a></li>
        </ul>
      </div>
      <div class="brand-section">
        <BrandComponent />
      </div>

      <div class="system-section">
        <SystemComponent />
      </div>
    </div>
  </div>
</template>

<script>
import AppHeader from "@/components/global/AppHeader.vue";
import BrandComponent from "@/components/BrandComponent.vue";
import SystemComponent from "@/components/SystemComponent.vue";
export default {
  name: "ShopView",
  components: {
    BrandComponent,
    SystemComponent,
    AppHeader
  },
};
</script>

<style lang="scss" scoped>
.shop {
  padding: 20px;
  //   background-color: #eee;
  .brand-section {
    margin-top: 10%;
  }

  .system-section {
    margin-top: 8%;
  }
  h1 {
    margin-bottom: 50px;
    font-size: 50px;
  }
  .container {
    // border: 2px solid blue;

    ul {
      li {
        display: inline-block;
        margin: 0 20px;

        a {
          text-decoration: none;
          font-size: 10px;
          text-transform: uppercase;
          color: #000;
        }
      }
    }
  }
}

@media screen and (max-width: 1024px) {
  .shop {
    h1 {
      margin-bottom: 50px;
      margin-top: 60px;
      font-size: 50px;
      // border:2px solid;
    }
    .container {
      // border: 2px solid;
      // width: 460px;

      ul {
        display: flex;
        flex-direction: column;
        li {
          padding: 10px;
          margin: 5px 0px;
          a {
            font-size: 13px;
          }
        }
      }
    }
  }
}
</style>
