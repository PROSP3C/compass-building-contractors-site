<script lang="ts" setup>
  export interface ContentSectionProps {
    sectionTitle: string
    paragraphs: string[]
    dark?: boolean
  }

  withDefaults(defineProps<ContentSectionProps>(), {
    sectionTitle: '',
    paragraphs: () => [''],
    dark: true,
  })
</script>

<template>
  <div
    class="ContentSection"
    :class="dark ? 'dark' : 'light'"
  >
    <h2>{{ sectionTitle }}</h2>

    <p
      v-for="(paragraph, i) in paragraphs"
      :key="i"
    >
      {{ paragraph }}
    </p>
  </div>
</template>

<style lang="scss" scoped>
  .ContentSectioon {
    &.dark {
      background: $primary;
      color: #fff;
    }

    &.light {
      background: #fff;
      color: $primary;
    }
  }
</style>
