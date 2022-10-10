<template>
  <div class="brand">
    <div class="container">
      <div class="brand-strategy">
        <h2>Brand Strategy Tools</h2>
        <p>
          Whether you are working remotely or in-person our brand strategy tools
          equip you to run a successful brand strategy workshop that delivers
          results and engages participants to contribute their best.
        </p>
      </div>

      <div class="brand-cards">
        <BrandCard
          spanHead="Print"
          title="Brand Cards"
          pargraph="Ideation tool for brand strategists, designers, and creative teams to create mood boards and transform ideas into brand or design concepts."
          price="$160"
        />

        <BrandCard
          spanHead="Digital"
          title="Brand Canvas (Digital)"
          pargraph="Brand Canvas provides a structure and ideation cards to distill your ideas, narrow in on your vision, and crystallize your brand essence. It’s your surfboard for catching the next wave of success."
          price="$175"
        />

        <BrandCard
          spanHead="Digital"
          title="Brand Experience Design Framework"
          pargraph="This framework provides a structure and a set of tools to create and activate an experience that your customer goes through as they are developing a relationship with your brand."
          price="$1,300.00"
        />

        <BrandCard
          spanHead="Digital"
          title="Brand Strategy Framework"
          pargraph="This framework provides a tried-and-true process and a set of tools to jump-start the creation of a brand system that positions you as the leader in the space, reinforces your authenticity, and grabs your audiences attention."
          price="$1,100.00"
        />

        <BrandCard
          spanHead="Digital"
          title="Brand Strategist Toolkit"
          pargraph="These ideation cards will enable you to gamify your workshops, smoothen your conversations, explore visual trends and best practices, as well as add more play to your work!"
          price="$2,900.00"
          class="toolkit"
        />
      </div>
    </div>
  </div>
</template>

<script>
import BrandCard from "@/components/BrandCard.vue";
export default {
  name: "BrandComponent",
  components: {
    BrandCard,
  },
};
</script>

<style lang="scss" scoped>
.brand {
  .container {
    max-width: 1500px;
    // border: 2px solid;
    // padding:0;
    .brand-strategy {
      display: flex;
      justify-content: space-between;
      align-items: center;
      // border:2px solid red;

      h2 {
        max-width: 50%;
        font-size: 40px;
        text-align: left;
        text-transform: capitalize;
        padding: 15px 0px;
        border-bottom: 8px solid #74ddda;
      }

      p {
        max-width: 30%;
        word-wrap: break-word;
        text-align: left;
        line-height: 30px;
      }
    }

    .brand-cards {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      margin-top: 3%;
      // border:2px solid blue;

      .toolkit {
        max-width: 100%;
        // border:2px solid;
      }
    }
  }
}

@media screen and (max-width: 1024px) {
  .brand {
    .container {
      .brand-strategy {
        flex-direction: column;
        margin-bottom: 20%;

        h2 {
          max-width: 100%;
          margin-bottom: 50px;
        }

        p {
          max-width: 100%;
        }
      }
    }
  }
}


</style>
