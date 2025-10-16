<template>
  <div class="PageHero"></div>
</template>

<style lang="scss" scoped>
  .PageHero {
    background-image: url('/working.jpg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    height: 150px;
    border-bottom: 5px solid $secondary;

    @include respond-to('sm') {
      height: 200px;
    }

    @include respond-to('md') {
      height: 250px;
    }

    @include respond-to('lg') {
      height: 300px;
    }
  }
</style>
