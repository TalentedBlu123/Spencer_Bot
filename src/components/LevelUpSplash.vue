<!-- LevelUpSplash.vue -->
<template>
  <div class="level-up-splash" v-if="showSplash">
    <img src="../assets/lvlup.jpg" alt="Level Up Image">
  </div>
</template>

<script>
export default {
  props: {
    showSplash: Boolean
  }
};
</script>

<style scoped>
.level-up-splash {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 9999;
}

.level-up-splash img {
  width: 200px;
  height: auto;
  transition:0.7s;

}

</style>
