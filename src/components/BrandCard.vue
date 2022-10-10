<template>
  <div class="brand-content">
    <span class="print">{{ spanHead }}</span>
    <h3>{{ title }}</h3>
    <p>{{ pargraph }}</p>

    <span class="price">{{ price }}</span>
    <button>learn more</button>
  </div>
</template>

<script>
export default {
  name: "BrandCard",
  props: ["spanHead", "title", "pargraph", "price"],
};
</script>

<style lang="scss" scoped>
.brand-content {
  padding: 30px;
  text-align: left;
  background-color: #e9e9e9;
  margin-right: 10px;
  margin-bottom: 50px;
  max-width: 48%;
  border-radius: 5px;
  .print {
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

  .price {
    margin-bottom: 10px;
    margin-top: 40px;
    display: block;
    font-size: 30px;
  }
  button {
    display: block;
    background-color: #000;
    color: #fff;
    padding: 15px 25px;
    border: none;
    font-size: 18px;
    cursor: pointer;
    text-transform: capitalize;
  }
}

@media screen and (max-width: 1024px) {
  .brand-content {
    max-width: 100%;
    margin-right: 0;
  }
}


// @media screen and (max-width: 1024px) {
//   .brand-content {
//     max-width: 100%;
//     margin-right: 0;
//   }
// }
</style>
