<script lang="ts" setup>
  import ContentSection from 'src/components/ContentSection.vue'
  import PageHero from 'src/components/PageHero.vue'
</script>

<template>
  <div>
    <PageHero />
    <ContentSection
      section-title="PROJECTS"
      :paragraphs="[
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut nec mauris lectus. Nulla rutrum tellus ipsum, nec dignissim sapien rhoncus finibus. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque vitae venenatis lectus. Nam ac elementum risus. Phasellus quis metus purus. Suspendisse nec arcu id leo fringilla auctor. Donec tempor sodales massa, sit amet fringilla velit bibendum id.',
      ]"
      :dark="false"
    />
  </div>
</template>
