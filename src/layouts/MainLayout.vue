<script lang="ts" setup>
  import { ref } from 'vue'

  const mobileMenuOpen = ref(false)

  const toggleMobileMenu = () => {
    mobileMenuOpen.value = !mobileMenuOpen.value
  }
</script>

<template>
  <q-layout
    class="MainLayout"
    view="hHh lpR fFf"
  >
    <q-header
      elevated
      class="bg-primary text-white"
      height-hint="98"
    >
      <q-toolbar>
        <q-toolbar-title>
          <q-item
            clickable
            tag="a"
            href="/"
          >
            <q-avatar>
              <img
                src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg"
              />
            </q-avatar>
            &nbsp;Title
          </q-item>
        </q-toolbar-title>

        <q-btn
          class="MainLayout-mobileMenu"
          dense
          flat
          round
          icon="menu"
          @click="toggleMobileMenu"
        />
      </q-toolbar>

      <q-tabs
        class="MainLayout-desktopMenu"
        align="right"
      >
        <q-route-tab
          to="/about"
          label="ABOUT"
        />
        <q-route-tab
          to="/services"
          label="SERVICES"
        />
        <q-route-tab
          to="/projects"
          label="PROJECTS"
        />
        <q-route-tab
          to="/contact"
          label="CONTACT"
        />
      </q-tabs>
    </q-header>

    <q-drawer
      show-if-above
      v-model="mobileMenuOpen"
      side="right"
    >
      <q-list style="min-width: 100px">
        <q-item
          clickable
          tag="a"
          href="/about"
        >
          <q-item-section>ABOUT</q-item-section>
        </q-item>
        <q-item
          clickable
          tag="a"
          href="/services"
        >
          <q-item-section>SERVICES</q-item-section>
        </q-item>
        <q-item
          clickable
          tag="a"
          href="/projects"
        >
          <q-item-section>PROJECTS</q-item-section>
        </q-item>
        <q-item
          clickable
          tag="a"
          href="/contact"
        >
          <q-item-section>CONTACT</q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer
      elevated
      class="bg-grey-8 text-white"
    >
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-avatar>
          <div>Title</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<style lang="scss" scoped>
  .MainLayout {
    &-desktopMenu {
      display: none;

      @include respond-to('sm') {
        display: block;
      }
    }

    &-mobileMenu {
      display: block;

      @include respond-to('sm') {
        display: none;
      }
    }
  }
</style>
