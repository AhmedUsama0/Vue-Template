<template>
  <div id="app">
    <router-view />
    <FooterComponent />
  </div>
</template>

<script>
import FooterComponent from "./components/global/FooterComponent.vue";
export default {
  name: "App",
  components: { FooterComponent },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
