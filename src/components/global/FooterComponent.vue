<template>
  <footer>
    <div class="container">
      <div>
        <ul>
          <a href="" class="logo">Logo</a>
          <li><a href="">about</a></li>
          <li><a href="">success stories</a></li>
          <li><a href="">shop</a></li>
          <li><a href="">blog</a></li>
          <li><a href="">FAQs</a></li>
          <li><a href="">shipping & Returns</a></li>
          <li><a href="">Terms & Conditions</a></li>
          <li><a href="">privacy policy</a></li>
          <li><a href="">Get in touch</a></li>
        </ul>
      </div>
      <div>
        <ul>
          <span>brand strategy tools</span>
          <li><a href="">brand experience design framework</a></li>
          <li><a href="">brand strategy framework</a></li>
          <li><a href="">brand strategist toolkit</a></li>
          <li><a href="">brand strategy kit</a></li>
          <li><a href="">brand cards</a></li>
          <li><a href="">brand canvas</a></li>
          <li><a href=""></a></li>
        </ul>
        <ul>
          <span>Systems</span>
          <li><a href="">brand system</a></li>
          <li><a href="">content system</a></li>
          <li><a href="">digital system</a></li>
        </ul>
      </div>
      <div>
        <ul>
          <span>inspiration tools</span>
          <li><a href="">style cards vol. 1</a></li>
          <li><a href="">style cards vol. 2</a></li>
          <li><a href="">word cards</a></li>
          <li><a href="">inspiration card</a></li>
        </ul>

        <ul>
          <span>content strategy tools</span>
          <li><a href="">content strategy framework</a></li>
          <li><a href="">content strategy kit</a></li>
          <li><a href="">content cards</a></li>
          <li><a href="">content canvas</a></li>
        </ul>
      </div>
      <div>
        <ul>
          <span>workshops</span>
          <li><a href="">bloomerang</a></li>
          <li><a href="">next-generation brand, who are you?</a></li>
          <li><a href="">brand experience design workshop</a></li>
          <li><a href="">UX Fundamentals</a></li>
          <li><a href="">mentorship program</a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style lang="scss" scoped>
footer {
  // padding: 5px;
  margin-top: 10%;
  .container {
    // max-width: 1500px;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;

    .logo {
      padding: 10px;
      text-decoration: none;
      font-size: 30px;
      color: #2c3e50;
      margin-top: 7%;
      display: block;
      width: fit-content;
      //   border:2px solid;
    }
    span {
      // border:2px solid;
      padding: 10px;
      margin-top: 10%;
      display: block;
      margin-bottom: 5%;
      text-transform: uppercase;
      font-size: 11px;
    }

    ul {
      text-align: left;
      //   border:2px solid;

      li {
        padding: 10px;

        a {
          text-decoration: none;
          color: #000;
          text-transform: capitalize;
          font-size: 14px;
        }
      }
    }
  }
}

@media screen and(max-width:768px) {
  footer {
    padding: 10px;
    .container {
      div {
        grid-column-start: 1;
        grid-column-end: 5;
        // padding:20px;
      }
    }
  }
}
</style>
