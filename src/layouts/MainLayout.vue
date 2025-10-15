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
          href="/"
        >
          <q-item-section>HOME</q-item-section>
        </q-item>
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

    <q-footer class="MainLayout-footer">
      <div class="MainLayout-footerContent">
        <div>
          <q-avatar>
            <img src="/compass-logo-white.png" />
          </q-avatar>
          <hr />
          <q-list style="min-width: 100px">
            <q-item
              clickable
              tag="a"
              href="/"
            >
              <q-item-section>HOME</q-item-section>
            </q-item>
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
        </div>
        <div>
          <hr />
          <div>
            <a
              href="tel:01775670045"
              target="_blank"
              style="margin-bottom: 2rem; margin-right: 1rem"
            >
              <q-icon name="phone" />
              <span>01775 670045</span>
            </a>
            <a
              href="tel:07368957257"
              target="_blank"
              style="margin-bottom: 2rem"
            >
              <q-icon name="phone" />
              <span>07368957257</span>
            </a>
          </div>
          <a
            href="mailto:compass.buildingcontractors@gmail.com"
            target="_blank"
            style="margin-bottom: 2rem"
          >
            <q-icon name="email" />
            <span>compass.buildingcontractors@gmail.com</span>
          </a>
          <hr />
          <div>
            <a
              href="/privacy-policy"
              style="margin-bottom: 1rem; margin-right: 1rem"
            >
              Privacy Policy</a
            >
            <a
              href="/terms-of-use"
              style="margin-bottom: 1rem"
            >
              Terms Of Use
            </a>
          </div>

          <hr />
          <p>© 2025 Compass Building Contractors Ltd. All rights reserved.</p>
          <p>
            Website by
            <a
              href="www.linkedin.com/in/declan-possnett-59682bb8"
              target="_blank"
            >
              Declan Possnett
            </a>
          </p>
        </div>
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
      padding: 2rem 1rem;
      border-top: 5px solid $secondary;

      a {
        color: #fff;

        i {
          margin-right: 0.25rem;
        }
      }

      hr {
        margin: 2rem auto 2rem auto;

        @include respond-to('md') {
          margin: 0 0 2rem 0;
          display: none;
        }
      }

      .q-avatar {
        margin-bottom: 1rem;
        height: 200px;
      }

      .q-item {
        padding: 0;
      }

      .MainLayout-footerContent {
        max-width: $max-width;
        margin: auto;
        display: flex;
        flex-direction: column;
        text-align: center;

        div:first-of-type {
          @include respond-to('md') {
            display: flex;
            flex-direction: row;
            gap: 2rem;
            height: 100%;
            margin: auto 0;
          }
        }

        > div:nth-of-type(2) {
          @include respond-to('md') {
            display: flex;
            flex-direction: column;
            align-items: flex-end;
            height: 100%;
            margin: auto 0;

            a {
              display: inline;
            }
          }
        }

        @include respond-to('md') {
          flex-direction: row;
          align-items: flex-start;
          justify-content: space-between;
          text-align: left;
        }
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
