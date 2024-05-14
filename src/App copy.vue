<script setup>
import AnimatedButton from './components/AnimatedButton.vue';
import ProgressBar from './components/ProgressBar.vue';
import LevelUpSplash from './components/LevelUpSplash.vue';
</script>

<template>
  <div class="container">
    
    <h1><img src="./assets/droplet-nature.gif" alt="Clicks Icon" class="clicks-icon">{{ number }}</h1>
    <AnimatedButton @click="handleClick">Hydrate</AnimatedButton>
    <div class="flex-left">
      <ProgressBar :value="progress" />
    </div>
    <LevelUpSplash :showSplash="showSplash" />
    

  </div>
</template>

<script>
export default {
  components: {
    AnimatedButton,
    ProgressBar,
    LevelUpSplash
  },
  data() {
    return {
      number: 0,
      progress: 0,
      showSplash: false
    };
  },
  methods: {
    handleClick() {
      if (this.progress < 100) {
        this.number += 1;
        this.progress += 5; // Increase progress by 5%
      }
      else {
        this.progress = 1;
        this.showSplash = true; // Show splash image
        setTimeout(() => {
          this.showSplash = false; // Hide splash image after 2 seconds
        }, 2000);
      }
    }
  }
};
</script>

<style scoped>
header {
  line-height: 1.5;
}
.flex-left {
  display:flex;
  justify-content: left;
  width:100%;
}



@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
