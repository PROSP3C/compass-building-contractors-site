<script lang="ts" setup>
  import ContentSection from 'src/components/ContentSection.vue'
  import PageHero from 'src/components/PageHero.vue'
</script>

<template>
  <div>
    <PageHero />
    <ContentSection
      section-title="SERVICES"
      :sections="[
        {
          title:
            'Trusted building expertise across Bourne, Peterborough, Spalding & surrounding areas',
          paragraph: `At Compass Building Contractors Ltd, we specialise in transforming existing spaces with precision, care, and a commitment to quality. Whether you're upgrading your home, refreshing a commercial property, or tackling essential repairs, our experienced team delivers dependable results with full regulatory compliance and a personal touch. Kitchen & bathroom renovations, Loft & garage conversions, Home extensions, Structural alterations & repairs, Interior reconfigurations & finishes - you name it, we can do it.`,
        },
        {
          title: 'Home Renovations & Improvements',
          paragraph: `We help homeowners breathe new life into their properties. From stylish kitchen makeovers to seamless extensions, we tailor every project to suit your lifestyle and budget. We offer Office refurbishments & fit-outs, Retail & hospitality improvements, Industrial unit upgrades, Accessibility & safety compliance and Fire protection & remedial works and much more.`,
        },
        {
          title: 'Commercial & Industrial Works',
          paragraph: `We support businesses across Lincolnshire and Cambridgeshire with practical, compliant construction solutions. Whether you're refreshing a retail space or upgrading an office, we deliver with minimal disruption and maximum professionalism.`,
        },
        {
          title: 'Groundworks & External Enhancements',
          paragraph:
            'From foundations to finishing touches, our team ensures your property is built on solid ground and looks great from the outside in. Some of these services include Site preparation & excavation, Drainage & foundation works, Driveways, patios & paving, Fencing & boundary walls and Landscaping & external finishes.',
        },
        {
          title: 'Property Maintenance & Repairs',
          paragraph: `We offer reliable maintenance services for homeowners, landlords, and commercial property managers. Whether it's a one-off fix or a scheduled plan, we keep your property safe, functional, and looking its best.`,
        },
      ]"
      :dark="false"
    />
  </div>
</template>
