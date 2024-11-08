<template>
  <div class="container">
    <!-- Заголовок страницы -->
    <h2 class="section-title">Why Choose Project Glow Skin?</h2>

    <!-- Десктопная версия: два блока параллельно -->
    <div v-if="isDesktop" class="desktop-borders">
      <div class="border-why">
        <h3>Truly Personalized</h3>
        <p>
          We offer the most comprehensive skin health analysis on the market.
          Take a holistic approach to precision skincare.
        </p>
      </div>

      <div class="border-why">
        <h3>Science-Backed</h3>
        <p>
          Every recommendation is supported by scientific research, ensuring
          effectiveness and safety.
        </p>
      </div>
    </div>

    <!-- Мобильная версия: два блока один под другим -->
    <div v-else>
      <div class="border-why">
        <h3>Truly Personalized</h3>
        <p>
          We offer the most comprehensive skin health analysis on the market.
          Take a holistic approach to precision skincare.
        </p>
      </div>

      <div class="border-why">
        <h3>Science-Backed</h3>
        <p>
          Every recommendation is supported by scientific research, ensuring
          effectiveness and safety.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

// Определяем, является ли устройство десктопом
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
.container {
  text-align: center; /* Центрирует весь текст в контейнере */
}

.section-title {
  margin-bottom: 20px;
  font-size: 24px;
  font-weight: bold;
}

/* Базовый стиль для рамок */
.border-why {
  border: 2px solid #ddd;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 8px;
}

.border-why h3 {
  font-weight: bold;
}

.border-why p {
  font-weight: normal;
}

/* Мобильная версия */
@media screen and (max-width: 900px) {
  .border-why {
    text-align: center; /* Центрирование текста внутри рамок */
  }
}

/* Десктопная версия */
@media screen and (min-width: 901px) {
  .container {
    padding-left: 17vh;
    padding-right: 17vh;
  }
  .desktop-borders {
    display: flex;
    justify-content: space-around;
    gap: 20px;
    margin-bottom: 20px;
  }

  .border-why {
    width: 45%; /* Ширина каждой рамки — 30% */
    text-align: center;
  }
}
</style>
