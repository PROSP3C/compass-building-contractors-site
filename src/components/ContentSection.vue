<script lang="ts" setup>
  export interface ContentSectionProps {
    sectionTitle: string
    paragraphs: string[]
    dark?: boolean
    imageSrc?: string
  }

  withDefaults(defineProps<ContentSectionProps>(), {
    sectionTitle: '',
    paragraphs: () => [''],
    dark: true,
    imageSrc: '',
  })
</script>

<template>
  <div
    class="ContentSection"
    :class="dark ? 'dark' : 'light'"
  >
    <q-img
      v-if="imageSrc"
      height="50px"
      width="50px"
      :no-transition="true"
      :no-spinner="true"
      :ratio="1"
      :src="imageSrc"
    />

    <h2>{{ sectionTitle }}</h2>

    <hr />

    <p
      v-for="(paragraph, i) in paragraphs"
      :key="i"
    >
      {{ paragraph }}
    </p>

    <hr />
  </div>
</template>

<style lang="scss" scoped>
  .ContentSection {
    color: $primary;
    padding: 3rem 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;

    h2 {
      font-size: 3rem;

      @include respond-to('md') {
        font-size: 4rem;
      }
    }

    p {
      max-width: $max-width;
      margin: auto;
      margin-top: 1rem;
    }

    @include respond-to('md') {
      padding: 5rem 2rem;
    }

    &.dark {
      background: $primary;
      color: #fff;
    }

    &.light {
      background: #fff;
      color: $primary;

      hr {
        border-color: $secondary;
      }
    }
  }
</style>
