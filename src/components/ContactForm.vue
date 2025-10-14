<script lang="ts" setup>
  import { ref } from 'vue'

  const name = ref('')
  const phone = ref('')
  const message = ref('')
  const accept = ref(false)
</script>

<template>
  <q-form class="q-gutter-md">
    <h2>Contact Us</h2>

    <q-input
      filled
      v-model="name"
      label="Your name *"
      hint="Name and surname"
      lazy-rules
      :rules="[(val) => (val && val.length > 0) || 'Please type something']"
    />

    <q-input
      filled
      type="number"
      v-model="phone"
      label="Your age *"
      lazy-rules
      :rules="[
        (val) => (val !== null && val !== '') || 'Please type your age',
        (val) => (val > 0 && val < 100) || 'Please type a real age',
      ]"
    />

    <q-input
      filled
      v-model="message"
      label="Message *"
      lazy-rules
      :rules="[
        (val) =>
          (val !== null && val !== '') || 'Please type your phone number',
        (val) => (val > 0 && val < 100) || 'Please type a valid phone number',
      ]"
    />

    <q-toggle
      v-model="accept"
      label="I accept the license and terms"
    />

    <div>
      <q-btn
        class="flex full-width"
        label="Submit"
        type="submit"
        color="primary"
      />
    </div>
  </q-form>
</template>
