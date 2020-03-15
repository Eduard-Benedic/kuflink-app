<template>
  <div class="container grid-33 gap4">
    <Card v-for="(card, index) in cardArr" :key="index" v-bind:cardText="card" />
  </div>
</template>

<script>
import Card from "./Card";
import { gsap } from "gsap";
export default {
  name: "CardGrid",
  components: {
    Card
  },
  data() {
    return {
      cardArr: [
        {
          title: "Trusted investments for you",
          subtitle: "Join us today",
          description:
            "Fund exciting projects secured against UK property* and earn up to 7.2% interest per annum*, plus up to 4% cashback** on your first investment."
        },
        {
          title: "Trusted investments",
          subtitle: "Join us yesterday",
          description:
            "Fund exciting projects secured against UK property* and earn up to 7.2% interest per annum*, plus up to 4% cashback** on your first investment."
        },
        {
          title: "Trusted",
          subtitle: false,
          description:
            "Fund exciting projects secured against UK property* and earn up to 7.2% interest per annum*, plus up to 4% cashback** on your first investment."
        }
      ]
    };
  },
  mounted() {
    gsap
      .timeline()
      .from(".card", { x: 900, duration: 0.6, opacity: 0, stagger: 0.2 }, 1);
    console.log("card grid mounted");
  }
};
</script>

<style lang="scss">
</style>