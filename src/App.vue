<template>
  <div id="app">
    <div class="unit" v-for="unit in manifest" :key="unit.item">
      <start-somewhere :item="unit.item" :url="unit.url"></start-somewhere>
    </div>
  </div>
</template>

<script>
import StartSomewhere from "./components/Module/StartSomewhere.vue";

export default {
  components: {
    StartSomewhere,
  },
  data() {
    return {
      manifest: [
        {
          item: "backpack",
          url: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/backpack.jpg",
        },
        {
          item: "tshirt",
          url: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/tshirt.jpg",
        },
        {
          item: "sweatshirt",
          url: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/sweatshirt.jpg",
        },
      ],
    };
  },
};
</script>

<style lang="scss"></style>
