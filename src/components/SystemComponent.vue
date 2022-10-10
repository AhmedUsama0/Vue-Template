<template>
  <div class="system">
    <div class="container">
      <div class="systems">
        <h4>Systems</h4>
        <p>
          We provide plug-and-play systems that elevate your brands <br />
          experience driving sales.
        </p>
      </div>

      <div class="system-cards">
        <SystemCard
          spanHead="System"
          title="Brand System"
          pargraph="Narrow in on your vision, crystallize your offering, brands positioning, messaging, personality, and design direction. Gain clarity and focus for your next move."
          bottomImg="BottomImage1.webp"
          bottomAlt="bottomImage1"
          topImg="topImage1.webp"
          topAlt="topImage1"
        />
        <SystemCard
          spanHead="System"
          title="Content System"
          pargraph="Create a content system that drives qualified leads to your website, moves them to action, and inspires them to come back for more."
          bottomImg="BottomImage2.webp"
          bottomAlt="bottomImage2"
          topImg="topImage2.webp"
          topAlt="topImage2"
        />

        <SystemCard
          spanHead="System"
          title="Brand System"
          pargraph="Transform your service into a digital product. Add an additional revenue stream. Scale your business."
          bottomImg="BottomImage3.webp"
          bottomAlt="bottomImage3"
          topImg="topImage3.webp"
          topAlt="topImage3"
        />
      </div>
    </div>
  </div>
</template>

<script>
import SystemCard from "@/components/SystemCard.vue";
export default {
  name: "SystemComponent",
  components: {
    SystemCard,
  },
};
</script>

<style lang="scss" scoped>
.system {
  .container {
    max-width: 1500px;
    .systems {
      display:flex;
      align-items: center;
      justify-content: space-between;
      //   border: 2px solid;

      h4 {
        // border:2px solid;
        font-size: 40px;
        border-bottom: 8px solid #ff5746;
        padding-bottom: 10px;
      }
      p {
        padding-right: 50px;
        text-align: left;
        line-height: 25px;
      }
    }
  }

  .system-cards {
    display: flex;
    justify-content: space-between;
    margin-top: 3%;
  }
}

@media screen and (max-width: 1024px) {
  .system {
    .container {
      .systems {
        flex-direction: column;
        align-items: baseline;
        p {
          margin: 10% 0;
          line-height: 30px;
        }
      }
    }
    .system-cards {
      flex-direction: column;
    }
  }
}
</style>
