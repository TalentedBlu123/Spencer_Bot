<!-- ProgressBar.vue -->
<template>
    <div class="progress-bar" :style="{ width: value  + '%' }"></div>
</template>

<script>
export default {
  props: {
    value: Number
  }
};
</script>

<style scoped>
.progress-bar {
  height: 20px; /* Adjust height as needed */
  background-color:#13b1d9; /* Purple color */
  border-radius:10px;
  transition: width 0.3s ease; /* Smooth transition animation */
  margin: 1rem; /* Apply margin to both axes */
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3); /* Subtle shadow */
}
</style>
