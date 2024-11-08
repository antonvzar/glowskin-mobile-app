<template>
  <header class="header">
    <div class="container header-content">
      <!-- Логотип -->
      <div class="image-container">
        <img
          style="width: 50%"
          src="@/assets/images/GP-logo-Skin.svg"
          alt="Clickable Image"
          @click="handleClick"
        />
      </div>

      <!-- Навигация для десктопа -->
      <nav class="desktop-nav" v-if="isDesktop">
        <a href="#" class="btn btn-text">For Skin Care Taker</a>
        <a href="#" class="btn btn-text">For Business</a>
      </nav>

      <!-- Кнопки для всех устройств -->
      <nav class="btns">
        <button class="btn btn-text">For Business</button>
        <div>|</div>
        <button class="btn btn-text">Sign in</button>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const handleClick = () => {
  console.log('Image clicked!')
}

// Определение устройства: десктоп или мобильное
const isDesktop = ref(window.innerWidth >= 901)

const updateDevice = () => {
  isDesktop.value = window.innerWidth >= 901
}

onMounted(() => {
  window.addEventListener('resize', updateDevice)
})

onUnmounted(() => {
  window.removeEventListener('resize', updateDevice)
})
</script>

<style scoped>
.header {
  position: sticky;
  top: 0;
  background: linear-gradient(89.97deg, #f4f7f2 0.04%, #ffffff 99.98%);
  padding: 16px 0;
  padding-left: 17vh;
  padding-right: 17vh;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* Кнопки "For Skin Care Taker" и "For Business" для десктопа */
.desktop-nav {
  display: flex;
  gap: 10vw;
  margin-right: 30vw;
}

.nav-link {
  color: black;
  text-decoration: none;
  font-weight: 600;
  padding: 0 10px;
}

/* Основные стили для кнопок */
.btn-text {
  background: none;
  border: none;
  color: black;
  font-weight: 600;
  padding: 0;
  font-size: 1vw;
}

.nav-link {
  gap: 10vw;
}

.btns {
  display: flex;
  gap: 5px;
}

.image-container {
  cursor: pointer;
}

/* Скрытие навигации для десктопа на мобильных устройствах */
@media screen and (max-width: 900px) {
  .desktop-nav {
    display: none;
  }
}
</style>
