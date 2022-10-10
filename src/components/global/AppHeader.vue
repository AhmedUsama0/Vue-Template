<template>
  <header :style="{ backgroundColor: background }">
    <div class="container-fluid">
      <label class="bars" for="toggle">
        <span></span>
        <span></span>
        <span></span>
      </label>
      <input type="checkbox" id="toggle" @click="test()" />
      <nav id="navbar">
        <div class="logo-close">
          <a href="" class="logo">Logo</a>
          <label for="close" class="cross"> &times; </label>
        </div>
        <input type="checkbox" id="close" @click="test()" />
        <ul>
          <router-link to="/" tag="li">
            <a href="">Shop</a>
          </router-link>

          <router-link to="/blog" tag="li">
            <a href="">Blog</a>
          </router-link>

          <router-link to="/signIn" tag="li">
            <a href="">Sign In</a>
          </router-link>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  props: ["background"],
  methods: {
    test: function () {
      var nav = document.getElementById("navbar");
      var close = document.getElementById("close");
      var toggle = document.getElementById("toggle");

      if (toggle.checked === true) {
        nav.style.left = 0 + "px";
        toggle.checked = false;
      } else if (close.checked === true) {
        nav.style.left = -1000 + "px";
        close.checked = false;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  .container-fluid {
    // width:1500px;
    .bars {
      padding: 0px 10px;
      display: none;
      cursor: pointer;
      &:hover {
        span {
          &:last-child {
            width: 30px;
          }
        }
      }
      span {
        height: 3px;
        display: block;
        width: 20px;
        margin-bottom: 3px;
        background-color: black;
        transition: 0.3s;

        &:not(:last-child) {
          width: 30px;
        }
      }
    }

    #toggle {
      display: none;
    }

    nav {
      transition: all 0.5s ease-in-out;
      display: flex;
      justify-content: space-between;
      align-items: center;

      .logo-close {
        .logo {
          text-decoration: none;
          font-size: 30px;
          color: #2c3e50;
        }

        .cross {
          display: none;
        }
      }

      #close {
        display: none;
      }

      ul {
        text-align: right;

        li {
          display: inline-block;
          padding: 0 25px;
          transition: 0.3s;

          &:hover {
            transform: translateX(-6px);
          }

          a {
            text-decoration: none;
          }
        }
      }
    }
  }
}

@media screen and(max-width:767px) {
  header {
    padding: 0;
    .container-fluid {
      position: relative;
      height: 30px;

      .bars {
        display: block;
        margin-top: 10px;
        padding: 10px 10px;
        position: absolute;
      }

      nav {
        background-color: #e9e9e9;
        width: 50%;
        display: block;
        padding: 0;
        height: 700px;
        position: absolute;
        left: -1000px;

        .logo-close {
          display: flex;
          justify-content: space-between;
          align-items: center;
          .cross {
            font-size: 40px;
            cursor: pointer;
            padding: 10px;
            margin-right: 2%;
            display: block;
          }

          .logo {
            padding-left: 10px;
            padding-top: 10px;
            text-align: left;
          }
        }

        ul {
          li {
            display: block;
            text-align: center;
            padding: 20px 0;
            border-bottom: 1px solid #fff;

            &:not(:last-child) {
              margin-bottom: 20px;
            }
          }
        }
      }
    }
  }
}
</style>
