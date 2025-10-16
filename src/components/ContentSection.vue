<script lang="ts" setup>
  type Section = {
    title: string
    paragraph: string
  }
  export interface ContentSectionProps {
    sectionTitle: string
    sections: Section[]
    dark?: boolean
    imageSrc?: string
  }

  withDefaults(defineProps<ContentSectionProps>(), {
    sectionTitle: '',
    paragraphs: () => [],
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
      style="margin-bottom: 1rem"
      :no-transition="true"
      :no-spinner="true"
      :ratio="1"
      :src="imageSrc"
    />

    <h2>{{ sectionTitle }}</h2>

    <hr v-if="sections.length" />

    <template
      v-for="({ title, paragraph }, i) in sections"
      :key="i"
    >
      <h3 v-if="title.length">{{ title }}</h3>

      <p>
        {{ paragraph }}
      </p>
    </template>

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
      max-width: $max-copy-width;
      text-align: center;

      @include respond-to('md') {
        font-size: 4rem;
      }
    }

    h3 {
      margin: 2rem auto 1rem auto;
      max-width: $max-copy-width;
      width: 100%;
      font-size: 2rem;
    }

    p {
      max-width: $max-copy-width;
      margin: auto;
      margin-top: 1rem;
      font-size: 1rem;
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
