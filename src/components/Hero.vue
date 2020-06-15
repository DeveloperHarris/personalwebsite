<template>
  <div class="hero">
    <img class="hero_image" src="../assets/spacex_hero.jpg" />
  </div>
</template>

<script>
export default {
  name: "Hero"
};
</script>

<style>
.hero {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;

  /* TODO: convert this to prop */
  height: 30vh; /* Height to display */
}

/* TODO: convert this to prop */
.hero_image {
  padding-top: 100px; /* Shift image "center" up by 100px */

  /* Gradually shifts image to left as screen gets smaller
   to keep face on screen */
  padding-right: calc(-15% + 200px);

  height: 375%; /* Vertical scale of image based on flexbox height */
}
</style>