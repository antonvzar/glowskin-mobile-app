<template>
  <div class="container">
    <!-- Фоновое изображение для мобильной версии -->
    <img
      v-if="!isDesktop"
      class="mobile-background-img"
      src="@/assets/images/shape-future.svg"
      alt="Background Image"
    />

    <!-- Первый раздел: Community Section -->
    <section class="community">
      <h2 class="section-title">Shape the Future of Skincare</h2>
      <p class="community-description">
        Join us in transforming skincare as we know it. Be part of a community
        that values innovation, science, and sustainability. Together, we can
        create a healthier, more radiant future for our skin.
      </p>
    </section>

    <!-- Второй раздел: Newsletter Section -->
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
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const email = ref('')
const isDesktop = ref(window.innerWidth > 900)

const subscribeNewsletter = () => {
  console.log('Subscribing email:', email.value)
  email.value = ''
}

const handleResize = () => {
  isDesktop.value = window.innerWidth > 900
}

onMounted(() => {
  window.addEventListener('resize', handleResize)
})

onUnmounted(() => {
  window.removeEventListener('resize', handleResize)
})
</script>

<style scoped>
/* Общие стили */
.section-subtitle {
  margin-top: 20px;
}

.container {
  display: flex;
  flex-direction: column;
  padding: 20px;
}

/* Мобильная версия */
.mobile-background-img {
  width: 100%;
  height: auto;
}

/* Стили для Community Section */
.community {
  margin-bottom: 40px;
  text-align: left;
}

.community-description {
  margin-bottom: 24px;
}

.section-title {
  font-size: 1.8em;
  font-weight: bold;
  margin-bottom: 16px;
}

/* Стили для Newsletter Section */
.newsletter {
  margin-bottom: 40px;
  text-align: left;
}

.privacy-note {
  font-size: 1.1em;
  color: var(--text-light);
  margin-top: 20px;
  color: black;
}

.newsletter-form {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.email-input {
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 25px;
}

.submit-btn {
  width: 100%;
}

/* Десктопная версия */
@media screen and (min-width: 901px) {
  .container {
    background-image: url('@/assets/images/shape-future.svg');
    background-size: cover;
    background-position: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 40px;
    height: 100vh;
    padding-left: 17vh;
    padding-right: 17vh;
  }

  .content {
    position: relative;
    margin-left: 50%;
    max-width: 50%;
    text-align: left;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .section-title {
    font-size: 2.4em;
  }

  .community-description,
  .privacy-note,
  .newsletter-form,
  .submit-btn {
    font-size: 1.1em;
  }
}
</style>
