<template>
  <div class="blog">
    <AppHeader background="#c2d4d4" />
    <div class="head">
      <div class="container">
        <h1>Finding Subject In Object: A Drink with Oleg Zaharevich</h1>
        <span class="arrow">➜</span>
      </div>
    </div>

    <div class="blog-cards">
      <div class="container">
        <div class="blog-card-container">
          <BlogCard
            header="How to use the Content Cards?"
            name="egle karalyte"
            category="tools"
            background="#e8e6d7"
            img="contentCards.webp"
          />
          <BlogCard
            header="Funky Old School"
            name="amy masterman"
            category="styles"
            background="#c2d4d4"
            img="funkySchool.webp"
          />
          <BlogCard
            header="Introducing Style Cards Vol. 1"
            name="egle karalyte"
            category="tools"
            background="#bbc9bd"
            img="styleCards.webp"
          />
          <BlogCard
            header="Mysticism in Design – A Conversation with Oksal Yesilok"
            name="tom simpson"
            category="talks on creativity"
            background="#c0b3c3"
            img="oksal.webp"
          />
          <BlogCard
            header="Brand Name Troubles? Make Naming Your Brand Easy, Effective, & Fun"
            name="alex koktsidis"
            category="brand strategy"
            background="#dbc4be"
            img="brandName.webp"
          />
          <BlogCard
            header="Thinking Beyond Today: What is the Greater Impact of a Brand?"
            name="amy masterman"
            category="brand strategy"
            background="#c0b3c3"
            img="thinking.webp"
          />
        </div>
      </div>
    </div>
    <div class="stay-with-us">
      <div class="container">
        <h4>Stay on the beat with us</h4>
        <input type="text" placeholder="Name" required />
        <input type="email" placeholder="Email" required />
        <button>Subscribe</button>
      </div>
    </div>
  </div>
</template>

<script>
import AppHeader from "@/components/global/AppHeader.vue";
import BlogCard from "@/components/BlogCard.vue";
export default {
  name: "BlogView",
  components: {
    BlogCard,
    AppHeader,
  },
};
</script>

<style lang="scss" scoped>
.blog {
  .head {
    background-color: #c2d4d4;
    min-height: 70vh;
    grid-template-columns: repeat(12, 1fr);

    .container {
      padding-top: 17vh;

      h1 {
        text-align: left;
        width: 50%;
        font-size: 60px;
        line-height: 75px;
        color: #000;
        font-weight: 500;
      }

      .arrow {
        display: block;
        width: fit-content;
        text-align: left;
        font-size: 50px;
        color: #000;
        transition: 0.5s;
        cursor: pointer;

        &:hover {
          transform: translateX(10px);
        }
      }
    }
  }

  .blog-cards {
    margin-top: 10%;
    .container {
      .blog-card-container {
        display: grid;
        grid-template-columns: 30% 30% 30%;
        justify-content: center;
        gap: 20px;
      }
    }
  }

  .stay-with-us {
    background-color: #000;
    padding: 200px 0px;
    margin-top: 100px;
    .container {
      //   border:2px solid;
      text-align: left;

      h4 {
        color: #fff;
        font-size: 30px;
        font-weight: normal;
      }

      input {
        margin: 50px 0px;
        background-color: #000;
        height: 30px;
        outline: none;
        border: none;
        border-bottom: 1px solid gray;
        font-size: 20px;
        color: #fff;

        &:nth-child(2) {
          margin-right: 50px;
        }
      }

      button {
        display: block;
        color: #000;
        background-color: #fff;
        padding: 22px 40px;
        font-size: 17px;
        cursor: pointer;
      }
    }
  }
}


@media (max-width:420px) {
  .blog .container {
    padding-top:20vh !important;
  }
}

@media screen and(max-width:767px) {
  .blog {
    .head {
      .container {
        padding-top:25vh;
        h1 {
          width: 100%;
          font-size: 32px;
        }

        .arrow {
          font-size: 45px;
        }
      }
    }

    .blog-cards {
      margin-top: 10%;
    }

    .stay-with-us {
      background-color: #000;
      padding: 200px 0px;
      margin-top: 100px;
      .container {
        max-width: 1000px;
        //   border:2px solid;
        text-align: left;

        h4 {
          color: #fff;
          font-size: 30px;
          font-weight: normal;
        }

        input {
          margin: 50px 0px;
          background-color: #000;
          height: 30px;
          outline: none;
          border: none;
          border-bottom: 1px solid gray;
          font-size: 20px;
          color: #fff;

          &:nth-child(2) {
            margin-right: 50px;
          }
        }

        button {
          display: block;
          color: #000;
          background-color: #fff;
          padding: 22px 40px;
          font-size: 17px;
          cursor: pointer;
        }
      }
    }
  }
}

@media (min-width:767px) {
  .blog h1 {
    font-size: 40px !important;
  }
}

@media (min-width:992px) {
  .blog h1 {
    font-size: 60px !important;
  }
}

</style>
