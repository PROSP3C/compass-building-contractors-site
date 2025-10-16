<script lang="ts" setup>
  import ContentSection from 'src/components/ContentSection.vue'
  import PageHero from 'src/components/PageHero.vue'
</script>

<template>
  <div>
    <PageHero />

    <ContentSection
      section-title="ABOUT US"
      :sections="[
        {
          title: 'Who Are We?',
          paragraph: `We are a friendly and family run building contractor company specialising in transforming existing spaces with precision, care, and a commitment to quality. Whether you're upgrading your home, refreshing a commercial property, or tackling essential repairs, our experienced team delivers dependable results with full regulatory compliance and a personal touch.`,
        },
        {
          title: 'Areas We Cover',
          paragraph: `We proudly serve clients in Bourne, Peterborough, Spalding, and surrounding towns and villages across Lincolnshire and Cambridgeshire. If you're nearby and unsure whether we cover your area, just reach out — we're always happy to help.`,
        },
      ]"
      :dark="false"
    />
  </div>
</template>
