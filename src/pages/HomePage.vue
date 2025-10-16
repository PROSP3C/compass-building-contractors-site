<script setup lang="ts">
  import ContentSection from 'src/components/ContentSection.vue'
  import HeroSection from 'src/components/HeroSection.vue'
</script>

<template>
  <q-page>
    <HeroSection />

    <ContentSection
      section-title="Welcome to Compass Building Contractors Ltd"
      :sections="[
        {
          title: '',
          paragraph: `At Compass Building Contractors Ltd, we believe great construction starts with trust, craftsmanship, and clear communication. With years of experience serving homeowners and businesses across Lincolnshire and Cambridgeshire, we’ve built a reputation for delivering high-quality work with a personal touch.`,
        },
        {
          title: '',
          paragraph: `Whether you're planning a home renovation, commercial upgrade, or essential property maintenance, our team brings precision, professionalism, and pride to every project. We don’t just build — we improve, restore, and enhance the spaces you rely on.`,
        },
      ]"
      image-src="bricks.png"
      :dark="true"
    />

    <ContentSection
      section-title="Local & Trusted"
      :sections="[
        {
          title: '',
          paragraph: `Based in the heart of Lincolnshire, we proudly serve clients in Bourne, Peterborough, Spalding, and surrounding towns and villages. Our team understands the local landscape, planning requirements, and expectations — giving you peace of mind from start to finish.`,
        },
        {
          title: '',
          paragraph: `Whether you're refreshing a family home or upgrading a business space, Compass Building Contractors Ltd is here to help. Get in touch today for a free consultation and discover how we can bring your project to life.`,
        },
      ]"
      image-src="houses.png"
      :dark="false"
    />
  </q-page>
</template>
