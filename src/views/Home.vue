<template>
  <div class="home">
    <LeafLetMap msg="A TreeMarkable Map"/>
  </div>
</template>

<script>
import LeafLetMap from "@/components/LeafLetMap.vue";

export default {
  name: "home",
  components: {
    LeafLetMap
  }
};
</script>

<style lang="scss" scoped>
.home {
  margin: 0;
  width: 100vw;
  height: 100vh;

  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
