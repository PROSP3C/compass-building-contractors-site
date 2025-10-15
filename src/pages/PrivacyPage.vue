<script lang="ts" setup>
  import ContentSection from 'src/components/ContentSection.vue'
</script>

<template>
  <div>
    <ContentSection
      section-title="Privacy Policy"
      :paragraphs="[
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut nec mauris lectus. Nulla rutrum tellus ipsum, nec dignissim sapien rhoncus finibus. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque vitae venenatis lectus. Nam ac elementum risus. Phasellus quis metus purus. Suspendisse nec arcu id leo fringilla auctor. Donec tempor sodales massa, sit amet fringilla velit bibendum id.',
        'Integer vulputate, ex et commodo placerat, leo massa maximus ipsum, ac consequat augue dolor vitae mauris. Fusce non placerat lectus. Vestibulum pellentesque vel est in maximus. Etiam sed lorem et nisi fringilla pretium id in felis. Phasellus eget tincidunt nisl, id pulvinar sapien. Quisque tincidunt urna nec mollis ultricies. Curabitur vel erat quis ex finibus tempor. Maecenas ac magna nisl. Curabitur fringilla quam vitae leo tempor, vel dapibus nibh suscipit. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; In ipsum erat, laoreet et gravida quis, lacinia nec odio. Sed eget varius magna. Duis eget ullamcorper lacus, a efficitur metus. Curabitur dapibus accumsan pharetra.',
      ]"
      :dark="false"
    />
  </div>
</template>
