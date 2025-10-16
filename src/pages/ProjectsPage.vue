<script lang="ts" setup>
  import ContentSection from 'src/components/ContentSection.vue'
  import PageHero from 'src/components/PageHero.vue'
</script>

<template>
  <div>
    <PageHero />
    <ContentSection
      section-title="PROJECTS"
      :sections="[
        {
          title: '',
          paragraph: `At Compass Building Contractors Ltd, we specialise in transforming existing spaces with precision, care, and a commitment to quality. Whether you're upgrading your home, refreshing a commercial property, or tackling essential repairs, our experienced team delivers dependable results with full regulatory compliance and a personal touch.`,
        },
      ]"
      :dark="false"
    />
  </div>
</template>
