<template>
  <header class="header">
    <div class="container header-content">
      <div class="image-container">
        <img
          style="width: 50%"
          src="@/assets/images/GP-logo-Skin.svg"
          alt="Clickable Image"
          @click="handleClick"
        />
      </div>
      <nav class="btns">
        <button class="btn btn-text">For business</button>
        <div>|</div>
        <button class="btn btn-text">Sign in</button>
      </nav>
    </div>
  </header>
</template>

<script setup>
const handleClick = () => {
  console.log('Image clicked!')
}
</script>

<style scoped>
.header {
  position: sticky;
  /* width: 100vw; */
  top: 0;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 16px 0;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 18px;
  font-weight: 700;
  color: black;
}

.btn-text {
  background: none;
  border: none;
  color: black;
  font-weight: 600;
  padding: 0;
}

.btns {
  display: flex;
  gap: 5px;
}

.image-container {
  cursor: pointer; /* Добавляем указатель, чтобы показать, что изображение кликабельно */
}
</style>
