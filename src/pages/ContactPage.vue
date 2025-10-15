<script lang="ts" setup>
  import ContactForm from 'src/components/ContactForm.vue'
  import PageHero from 'src/components/PageHero.vue'
</script>

<template>
  <div class="ContactPage">
    <PageHero />

    <div>
      <ContactForm />
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .ContactPage {
    div:nth-of-type(2) {
      padding: 1rem;
      max-width: $max-copy-width;
      margin: auto;
    }
  }
</style>
