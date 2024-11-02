<template>
  <section class="newsletter">
    <h3 class="section-subtitle">Follow Us for the Latest Updates</h3>
    <p class="privacy-note">
      Stay informed about new developments, tips, and product launches.
    </p>
    <form @submit.prevent="subscribeNewsletter" class="newsletter-form">
      <input
        type="email"
        v-model="email"
        placeholder="Your email address"
        class="email-input"
        required
      />
      <button type="submit" class="btn btn-primary submit-btn">
        Subscribe
      </button>
    </form>
    <h3 class="section-subtitle">Privacy Notice</h3>
    <p class="privacy-note">
      Your privacy is crucial to us. We are committed to protecting your
      personal information with the highest standards of security.
    </p>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')

const subscribeNewsletter = () => {
  // Implement newsletter subscription logic here
  console.log('Subscribing email:', email.value)
  // Reset the email input after submission
  email.value = ''
}
</script>

<style scoped>
.newsletter {
  margin-bottom: 40px;
}

.privacy-note {
  font-size: 14px;
  color: var(--text-light);
  margin-bottom: 16px;
}

.newsletter-form {
  display: flex;
  flex-direction: column;
}

.email-input {
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 25px;
  margin-bottom: 12px;
}

.submit-btn {
  width: 100%;
}
</style>
