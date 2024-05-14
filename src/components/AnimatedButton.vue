<template>
  <button class="bubbly-button" @click="showAnime">
    <slot></slot>
  </button>
</template>

<script setup>
const showAnime = (e) => {
    e.preventDefault();
    e.target.classList.remove('animate');
    // This line queues the class addition for the next DOM update cycle
    setTimeout(() => e.target.classList.add('animate'), 100);
};  

</script>

<style scoped lang="scss">
@import '../assets/AnimatedButton.scss';
</style>