<template>
  <div class="HeroSection">
    <h1>GUIDING YOUR BUILD WITH PRECISION AND TRUST</h1>
    <q-btn
      to="/contact"
      color="primary"
      role="link"
    >
      <span>CONTACT US</span>
      <q-icon name="send" />
    </q-btn>
  </div>
</template>

<style lang="scss" scoped>
  .HeroSection {
    background-image: url('/assets/hero.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    height: 600px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 0 1rem;
    border-bottom: 5px solid $secondary;

    @include respond-to('sm') {
      padding: 0 3rem;
    }

    h1 {
      color: #fff;
      text-align: center;
      font-weight: bold;
      margin: 0;
      font-size: 2.5rem;

      @include respond-to('md') {
        font-size: 4rem;
        max-width: 700px;
      }
    }

    a {
      font-size: 1.5rem;
      margin-top: 4rem;

      @include respond-to('md') {
        font-size: 2rem;
      }

      i {
        color: $secondary;
        margin-left: 1rem;
        font-size: 2rem;

        @include respond-to('md') {
          font-size: 3rem;
        }
      }
    }
  }
</style>
