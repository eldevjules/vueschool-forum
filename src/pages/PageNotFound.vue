<template>
  <div class="col-full"
       :class="$style.centered"
  >
    <h1 :class="$style.headingLarge">Not Found</h1>
    <p class="text-large"
       :class="$style.textLarge"
    >
      Oooooops! porque no mejor te vas al Home?
      <router-link :to="{name: 'Home'}">
        Home
      </router-link>
    </p>
  </div>
</template>

<script>
  export default {

  }
</script>

<style module>
  .headingLarge {
    font-size: 100px;
  }
  .textLarge {
    font-size: 50px;
    font-weight: 100;
  }
  .centered {
    text-align: center;
  }
</style>
