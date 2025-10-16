<script lang="ts" setup>
  import PageHero from 'src/components/PageHero.vue'
  import ContentSection from 'src/components/ContentSection.vue'
  import ContactForm from 'src/components/ContactForm.vue'
</script>

<template>
  <div class="ContactPage">
    <PageHero />

    <ContentSection
      section-title="CONTACT US"
      :paragraphs="[]"
      :dark="false"
      style="margin-bottom: -5rem"
    />

    <div class="ContactPage-contactOptions">
      <h4>Visit us on Facebook</h4>
      <q-btn
        href="https://www.facebook.com/profile.php?id=61581959920519"
        icon="facebook"
        label="Compass Building Contractors"
      />
      <h4>Give us a call</h4>

      <q-btn
        href="tel:01775670045"
        icon="phone"
        style="margin-bottom: 2rem; margin-right: 1rem"
        label="01775 670045"
      />
      <q-btn
        href="tel:07368957257"
        icon="phone"
        style="margin-bottom: 2rem; margin-right: 1rem"
        label="07368957257"
      />

      <h4>Or complete the form below:</h4>
    </div>

    <div>
      <ContactForm />
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .ContactPage {
    color: $primary;

    div {
      &:not(:first-child) {
        &:not(div:nth-of-type(2)) {
          padding: 1rem;
          max-width: $max-copy-width;
          margin: auto;
        }
      }
    }

    &-contactOptions {
      display: flex;
      flex-direction: column;
      gap: 1rem;

      h4 {
        margin-top: 2rem;
      }

      a {
        margin-bottom: 0 !important;
      }
    }
  }
</style>
