<template>
  <section class="features">
    <div class="desktop-layout" v-if="isDesktop">
      <!-- Левая часть с изображением -->
      <img class="img-container" src="@/assets/images/ai-girl-2.svg" />

      <!-- Правая часть с текстом и колонками -->
      <div class="text-content">
        <!-- Первый блок с заголовком и двумя колонками -->
        <h2 class="section-title">Science-Backed Ingredient Recommendations</h2>
        <p class="features-description">
          Our platform analyzes your unique skin profile and educates you on the
          scientific effects of each ingredient, ensuring you achieve your
          skincare goals with precision and understanding.
        </p>

        <div class="column-container">
          <div class="column">
            <img class="feature-image" src="@/assets/images/honeycomb.svg" />
            <div>
              <h3 class="feature-title">Ingredient-Led Solutions</h3>
              <p class="feature-description">
                Discover products containing specific ingredients that benefit
                your skin, demystifying common skincare myths with scientific
                backing.
              </p>
            </div>
          </div>

          <div class="column">
            <img class="feature-image" src="@/assets/images/unbiased.svg" />
            <div>
              <h3 class="feature-title">Unbiased, Factual Data</h3>
              <p class="feature-description">
                We integrate information from scientific papers, publications,
                and credible databases to provide you with reliable and unbiased
                skincare information.
              </p>
            </div>
          </div>
        </div>

        <!-- Второй блок с заголовком и двумя колонками -->
        <h2 class="section-title">Product Recommendation Engine</h2>
        <p class="features-description">
          Enhance your skincare routine with our ingredient-focused
          recommendation engine.
        </p>

        <div class="column-container">
          <div class="column">
            <img class="feature-image" src="@/assets/images/skincare.svg" />
            <div>
              <h3 class="feature-title">Tailored Product Suggestions</h3>
              <p class="feature-description">
                Find products that contain essential ingredients needed to
                achieve your skincare goals.
              </p>
            </div>
          </div>

          <div class="column">
            <img
              class="feature-image"
              src="@/assets/images/shopping-cart.svg"
            />
            <div>
              <h3 class="feature-title">Marketplace Integration</h3>
              <p class="feature-description">
                Shop directly from our platform, where we offer a curated
                selection of products that will help you glow from the inside
                out.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Мобильная версия с последовательным отображением и центрированием текста -->
    <div v-else>
      <img class="img-container" src="@/assets/images/ai-girl-2.svg" />

      <!-- Первый блок для мобильной версии -->
      <h2 class="section-title text-center">
        Science-Backed Ingredient Recommendations
      </h2>
      <p class="features-description text-center">
        Our platform analyzes your unique skin profile and educates you on the
        scientific effects of each ingredient, ensuring you achieve your
        skincare goals with precision and understanding.
      </p>

      <div class="feature-item">
        <img class="feature-image" src="@/assets/images/honeycomb.svg" />
        <div>
          <h3 class="feature-title">Ingredient-Led Solutions</h3>
          <p class="feature-description">
            Discover products containing specific ingredients that benefit your
            skin, demystifying common skincare myths with scientific backing.
          </p>
        </div>
      </div>

      <div class="feature-item">
        <img class="feature-image" src="@/assets/images/unbiased.svg" />
        <div>
          <h3 class="feature-title">Unbiased, Factual Data</h3>
          <p class="feature-description">
            We integrate information from scientific papers, publications, and
            credible databases to provide you with reliable and unbiased
            skincare information.
          </p>
        </div>
      </div>

      <!-- Второй блок для мобильной версии -->
      <h2 class="section-title text-center">Product Recommendation Engine</h2>
      <p class="features-description text-center">
        Enhance your skincare routine with our ingredient-focused recommendation
        engine.
      </p>

      <div class="feature-item">
        <img class="feature-image" src="@/assets/images/skincare.svg" />
        <div>
          <h3 class="feature-title">Tailored Product Suggestions</h3>
          <p class="feature-description">
            Find products that contain essential ingredients needed to achieve
            your skincare goals.
          </p>
        </div>
      </div>

      <div class="feature-item">
        <img class="feature-image" src="@/assets/images/shopping-cart.svg" />
        <div>
          <h3 class="feature-title">Marketplace Integration</h3>
          <p class="feature-description">
            Shop directly from our platform, where we offer a curated selection
            of products that will help you glow from the inside out.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isDesktop = ref(window.innerWidth > 900)

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
.features {
  background: linear-gradient(89.97deg, #f4f7f2 0.04%, #ffffff 99.98%);
  padding: 20px;
}

.img-container {
  width: 90vw;
  height: 80vw;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

/* Десктопная версия */
@media screen and (min-width: 901px) {
  .features {
    padding-left: 17vh;
    padding-right: 17vh;
  }
  .desktop-layout {
    display: flex;
    flex-direction: row;
  }

  .img-container {
    width: 40vw;
    height: 40vw;
  }

  .text-content {
    width: 50%;
    padding-left: 20px;
  }

  .column-container {
    display: flex;
    justify-content: space-between;
    margin-top: 20px;
  }

  .column {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    width: 48%;
    gap: 15px;
  }

  .feature-image {
    width: 10vw;
    margin-right: 15px;
  }

  .feature-title {
    font-size: 16px;
    font-weight: 600;
  }

  .feature-description {
    font-size: 14px;
    color: var(--text-light);
  }
}

/* Мобильная версия */
@media screen and (max-width: 900px) {
  .text-center {
    text-align: center;
  }

  .feature-item {
    display: flex;
    align-items: flex-start;
    margin-bottom: 20px;
    flex-direction: row;
  }

  .feature-image {
    width: 10vw;
    margin-right: 2vw;
  }
}
</style>
