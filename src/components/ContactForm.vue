<script lang="ts" setup>
  import { ref } from 'vue'

  const name = ref('')
  const phone = ref('')
  const message = ref('')
  const accept = ref(false)
</script>

<template>
  <q-form
    class="ContactForm q-gutter-md"
    netlify
    name="contact-form"
    method="post"
    data-netlify="true"
    data-netlify-honeypot="bot-field"
  >
    <h2>CONTACT US</h2>

    <input
      type="hidden"
      name="form-name"
      value="contact-form"
    />

    <q-input
      filled
      v-model="name"
      name="name"
      label="Your full name *"
      lazy-rules
      :rules="[(val) => (val && val.length > 0) || 'Please type your name']"
    />

    <q-input
      filled
      type="tel"
      v-model="phone"
      name="phone"
      label="Your contact number *"
      lazy-rules
      :rules="[
        (val) => !!val || 'Please type your contact number',
        (val) =>
          /^(\+44\s?7\d{3}|\(?07\d{3}\)?)\s?\d{3}\s?\d{3}$/.test(val) ||
          /^(\+44\s?1\d{1,3}|\(?01\d{1,3}\)?)\s?\d{3,4}\s?\d{3,4}$/.test(val) ||
          'Enter a valid UK phone number',
      ]"
    />

    <q-input
      filled
      type="textarea"
      v-model="message"
      name="message"
      label="Your message *"
      lazy-rules
      :rules="[(val) => (val && val.length > 0) || 'Please type your message']"
    />

    <q-toggle
      v-model="accept"
      label="I accept the license and terms"
    />

    <div>
      <q-btn
        class="flex full-width"
        label="Send"
        type="submit"
        color="primary"
      />
    </div>
  </q-form>
</template>

<style lang="scss" scoped>
  .ContactForm {
    color: $primary;
    margin-bottom: 3rem;

    @include respond-to('md') {
      margin-bottom: 5rem;
    }

    h2 {
      font-size: 3rem;
      text-align: center;
      margin-top: 3rem;

      @include respond-to('md') {
        font-size: 4rem;
        margin-top: 5rem;
        margin-bottom: 2rem;
      }
    }
  }
</style>
