<template>
  <div class="sign-in">
    <AppHeader />
    <div class="sign-in-content">
      <div class="container">
        <h1>My account</h1>
        <h2>Login</h2>
        <form action="">
          <div class="inputs">
            <label for="username">Username or email address</label>
            <input type="text" id="username" />
            <label for="password" class="password">Password</label>
            <input type="password" id="password" />
            <button type="submit">Log in</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import AppHeader from "@/components/global/AppHeader.vue";
export default {
  name: "SignInView",
  components: {
    AppHeader,
  },
};
</script>

<style lang="scss" scoped>
.sign-in {
  .sign-in-content {
    margin-top: 10vh;
    margin-bottom: 320px;
    .container {
      // border: 2px solid blue;

      .inputs {
        //   border:2px solid red;
        max-width: 500px;
        margin-left: auto;
        margin-right: auto;
        padding-left: 20px;
        margin-top: 100px;
        label,
        input {
          display: block;
        }

        label {
          text-align: left;
          font-size: 22px;
        }

        .password {
          margin-top: 60px;
        }

        input {
          width: 80%;
          border: none;
          border-bottom: 1px solid gray;
          margin-top: 20px;
          outline: none;
          padding:10px;
          font-size: 20px;
        }
      }

      h1 {
        font-size: 50px;
        font-weight: normal;
      }

      h2 {
        margin-top: 30px;
        font-size: 40px;
        font-weight: normal;
      }
    }
  }

  button {
    display: block;
    margin-top: 50px;
    background-color: #000;
    color: #fff;
    padding: 10px 17px;
    cursor: pointer;
  }
}
</style>
