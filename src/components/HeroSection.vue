<template>
  <div class="contain-background">
    <div class="content-wrapper">
      <div class="img-container"></div>
      <section class="hero">
        <p class="hero-description">Discover Your Skin's Perfect Match</p>
        <h1 class="hero-title">Precision Skincare Tailored for You</h1>
        <p class="hero-description">
          Our AI-powered analysis reveals what your skin truly needs to look and
          feel its best.
        </p>
        <button class="btn-primary">Your Free Skin Analysis Now</button>
        <p class="secure-note">Receive Personalized Recommendations</p>
        <p class="secure-note">100% Secure & Private</p>
      </section>
    </div>
  </div>
</template>

<style scoped>
/* Общие стили */
.contain-background {
  background: linear-gradient(89.97deg, #f4f7f2 0.04%, #ffffff 99.98%);
  padding: 20px;
}

.content-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}

@media screen and (max-width: 900px) {
  .content-wrapper {
    flex-direction: column;
  }

  .img-container {
    width: 90vw;
    height: 80vw;
    background-image: url('@/assets/images/girl-in-circle.svg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  .hero {
    text-align: center;
  }

  .hero-title {
    font-size: 28px;
    font-weight: 700;
    margin-bottom: 16px;
  }

  .hero-description,
  .secure-note {
    margin-bottom: 24px;
  }
}

@media screen and (min-width: 901px) {
  .content-wrapper {
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }

  .img-container {
    width: 57vh;
    height: 50vh;
    background-image: url('@/assets/images/girl-in-circle.svg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    margin-right: 20px;
  }

  .hero {
    max-width: 30vw;
    text-align: center;
  }

  .hero-title {
    font-size: 2vw;
    font-weight: 700;
    margin-bottom: 16px;
  }

  .hero-description,
  .secure-note {
    margin-bottom: 24px;
  }
}
</style>
