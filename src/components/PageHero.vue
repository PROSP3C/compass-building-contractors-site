<template>
  <div class="PageHero"></div>
</template>

<style lang="scss" scoped>
  .PageHero {
    background-image: url('/working.jpg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    height: 200px;
    border-bottom: 5px solid $secondary;

    @include respond-to('sm') {
      height: 300px;
    }

    @include respond-to('md') {
      height: 400px;
    }
  }
</style>
