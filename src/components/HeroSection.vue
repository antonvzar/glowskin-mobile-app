<template>
  <div class="background-img"></div>
  <section class="hero text-center">
    <p class="hero-description">Discover Your Skin's Perfect Match</p>
    <h1 class="hero-title">Precision Skincare Tailored for You</h1>
    <p class="hero-description">
      Our AI-powered analysis reveals what your skin truly needs to look and
      feel its best.
    </p>
    <button class="btn-primary">Your Free Skin Analysis Now</button>
    <p class="secure-note">Recieve Personalized Recommendations</p>
    <p class="secure-note">100% Secure & Private</p>
  </section>
</template>

<style scoped>
.hero {
  margin-bottom: 40px;
}

.hero-title {
  font-size: 28px;
  font-weight: 700;
  margin-bottom: 16px;
}

.hero-subtitle {
  font-size: 22px;
  font-weight: 600;
  margin-bottom: 12px;
}

.hero-description {
  margin-bottom: 24px;
}

.secure-note {
  font-size: 14px;
  color: var(--text-light);
  margin: 16px 0 24px;
}

.discover-title {
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 16px;
}

.background-img {
  width: 100%;
  height: 300px; /* Устанавливаем нужную высоту */
  background-image: url('@/assets/images/girl-in-circle.png'); /* Указываем путь к изображению */
  background-size: cover;
  background-position: center;
  margin: 20px;
}
</style>
