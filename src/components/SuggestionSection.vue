<template>
  <section class="features">
    <h2 class="section-title">Science-Backed Ingredient Recommendations</h2>
    <p class="features-description">
      Our platform analyzes your unique skin profile and educates you on the
      scientific effects of each ingredient, ensuring you achieve your skincare
      goals with precision and understanding.
    </p>
    <div class="feature-item">
      <img class="feature-image" src="@/assets/images/honeycomb.png" />
      <div>
        <h3 class="feature-title">Ingredient-Led Solutions</h3>
        <p class="feature-description">
          Discover products containing specific ingredients that benefit your
          skin, demystifying common skincare myths with scientific backing.
        </p>
      </div>
    </div>
    <div class="feature-item">
      <img class="feature-image" src="@/assets/images/unbiased.png" />
      <div>
        <h3 class="feature-title">Unbiased, Factual Data</h3>
        <p class="feature-description">
          We integrate information from scientific papers, publications, and
          credible databases to provide you with reliable and unbiased skincare
          information.
        </p>
      </div>
    </div>
  </section>

  <section class="features">
    <h2 class="section-title">Product Recommendation Engine</h2>
    <p class="features-description">
      Enhance your skincare routine with our ingredient-focused recommendation
      engine
    </p>

    <div class="feature-item">
      <img class="feature-image" src="@/assets/images/skincare.png" />
      <div>
        <h3 class="feature-title">Tailored Product Suggestions</h3>
        <p class="feature-description">
          Find products that contain essential ingredients needed to achieve
          your skincare goals.
        </p>
      </div>
    </div>
    <div class="feature-item">
      <img class="feature-image" src="@/assets/images/shopping-cart.png" />
      <div>
        <h3 class="feature-title">Marketplace Integration</h3>
        <p class="feature-description">
          Shop directly from our platform, where we offer a curated selection of
          products that will help you glow from the inside out.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.features {
  margin-bottom: 40px;
}

.features-description {
  margin-bottom: 24px;
}

.feature-title {
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 8px;
}

.feature-description {
  font-size: 14px;
  color: var(--text-light);
  margin-bottom: 16px;
}

.feature-item {
  display: flex;
  align-items: flex-start;
  margin-bottom: 20px;
}

.feature-image {
  width: 15%;
  margin-right: 15px;
}
</style>
