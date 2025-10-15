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
    view="hhh lpR fff"
  >
    <q-header
      class="bg-white text-primary"
      height-hint="98"
    >
      <div>
        <q-toolbar>
          <q-toolbar-title>
            <q-item
              clickable
              tag="a"
              href="/"
              class="flex items-center"
              style="padding: 0.5rem 0; width: 300px !important"
            >
              <q-avatar>
                <img src="compass-logo.png" />
              </q-avatar>

              <div class="MainLayout-titleContainer">
                <h1>COMPASS</h1>
                <h2>BUILDING CONTRACTORS</h2>
              </div>
            </q-item>
          </q-toolbar-title>

          <div class="MainLayout-desktopContactInfo">
            <div>
              <a
                href="tel:01775670045"
                target="_blank"
              >
                <q-icon name="phone" />
                <span>01775 670045</span>
              </a>
              <a
                href="tel:07368957257"
                target="_blank"
              >
                <q-icon name="phone" />
                <span>07368957257</span>
              </a>
            </div>
            <a
              href="mailto:compass.buildingcontractors@gmail.com"
              target="_blank"
            >
              <q-icon name="email" />
              <span>compass.buildingcontractors@gmail.com</span>
            </a>
          </div>

          <q-btn
            class="MainLayout-mobileMenuButton"
            dense
            flat
            round
            icon="menu"
            style="font-size: 1.5rem"
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
      </div>
    </q-header>

    <q-drawer
      class="MainLayout-mobileMenu"
      :show-if-above="false"
      v-model="mobileMenuOpen"
      side="right"
    >
      <q-btn
        dense
        flat
        round
        icon="close"
        style="font-size: 1.5rem"
        @click="toggleMobileMenu"
      />
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

    <q-footer class="bg-grey-8 text-white">
      <div>
        <q-toolbar>
          <q-toolbar-title>
            <q-avatar>
              <img src="/compass-logo-white.png" />
            </q-avatar>
          </q-toolbar-title>
        </q-toolbar>
      </div>
    </q-footer>
  </q-layout>
</template>

<style lang="scss" scoped>
  .MainLayout {
    header {
      border-bottom: 5px solid $secondary;

      > div {
        margin: auto;
        max-width: $max-width;
      }
    }

    footer {
      > div {
        margin: auto;
        max-width: $max-width;
      }
    }

    .q-toolbar__title {
      display: block;

      @include respond-to('sm') {
        display: flex;
        align-items: center;
        justify-content: center;
      }

      @media screen and (min-width: 580px) {
        display: block;
        margin-top: 1rem !important;
        margin-bottom: -1.5rem;
      }
    }

    .q-avatar {
      height: 5rem;
      width: auto;
      margin-left: 0rem;

      @include respond-to('sm') {
        height: 6rem;
        margin-left: -0.5rem;
      }
    }

    &-titleContainer {
      display: flex;
      flex-direction: column;
      justify-items: center;
      height: 100%;
      gap: 0.25rem;

      @include respond-to('sm') {
        align-items: center;
      }

      > h1,
      h2 {
        display: none;

        @media screen and (min-width: 320px) {
          display: flex;
        }
      }
    }

    &-desktopContactInfo {
      display: none;

      @media screen and (min-width: 580px) {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        justify-items: center;
        margin-top: 2rem;
        gap: 0.25rem;

        > div {
          display: flex;
          justify-content: space-between;
          width: 100%;
        }

        a {
          text-decoration: none;
          color: $primary;

          span {
            text-decoration: underline;
          }
        }

        i {
          color: $secondary;
          margin-right: 0.25rem;
        }
      }
    }

    :deep(.MainLayout-mobileMenu) {
      padding: 0.9rem;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      color: $primary;
      fill: $primary;

      .q-list {
        display: flex;
        flex-direction: column;
        width: 100%;
        margin-top: 2rem;
        font-size: 1.5rem;
        gap: 2rem;

        .q-tab__label {
          font-weight: bold !important;
        }
      }
    }

    h1 {
      font-size: 1.9rem;
      line-height: 1.5rem;
      font-weight: bold;
      margin: 0;

      @include respond-to('sm') {
        font-size: 2.1rem;
        line-height: 2.1rem;
      }

      @include respond-to('md') {
        font-size: 2.56rem;
        line-height: 2.56rem;
      }
    }

    h2 {
      font-weight: bold;
      margin: 0;
      font-size: 0.75rem;
      line-height: 0.75rem;

      @include respond-to('sm') {
        font-size: 0.8rem;
        line-height: 0.8rem;
      }

      @include respond-to('md') {
        font-size: 1rem;
        line-height: 1rem;
      }
    }

    &-desktopMenu {
      display: none;

      @include respond-to('sm') {
        display: block;
      }
    }

    &-mobileMenuButton {
      display: block;

      @include respond-to('sm') {
        display: none;
      }
    }
  }
</style>
