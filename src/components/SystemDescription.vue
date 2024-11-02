<template>
  <section class="why-choose-us">
    <img class="background_img" src="@/assets/images/ai-girl.png" />
    <h2 class="section-title">A New Era of Skincare</h2>
    <p class="features-description">
      Go beyond traditional surface-level assessments with personalized
      solutions that cater to every aspect of your skin's needs. Embrace a new
      era of skincare, precisely tailored to your unique biological blueprint
      and lifestyle.
    </p>
    <h3 class="section-subtitle">
      The Most Comprehensive Skin Health Analysis
    </h3>
    <ul class="feature-list">
      <li
        v-for="(feature, index) in features"
        :key="index"
        class="feature-item"
      >
        <img
          :src="getImageUrl(feature.imgsrc)"
          alt="Feature Image"
          class="feature-image"
        />

        <div>
          <h3 class="feature-title">{{ feature.title }}</h3>
          <p class="feature-description">{{ feature.description }}</p>
        </div>
      </li>
    </ul>
  </section>
</template>

<script setup>
import { CheckIcon } from 'lucide-vue-next'

const features = [
  {
    imgsrc: '@/assets/images/analysing.png',
    title: 'Extensively Trained',
    description:
      'Our technology has been trained on a diverse dataset of 100,000+ images to ensure high accuracy and reliability.',
  },
  {
    imgsrc: '@/assets/images/face-recognition.png',
    title: 'Image Recognition and Analysis',
    description:
      'Simply upload a selfie and our AI will instantly begin its detailed assessment, identifying and addressing key areas of concern with remarkable accuracy.',
  },
  {
    imgsrc: '@/assets/images/profile.png',
    title: 'Personalised Recommendations',
    description:
      "Sophisticated algorithms deliver precise product suggestions tailored to your skin's specific needs.",
  },
  {
    imgsrc: '@/assets/images/dna.png',
    title: 'Upload DNA Report',
    description:
      'Integrate genetic insights by uploading your DNA report, allowing us to refine your skincare recommendations based on your genetic predispositions.',
  },
  {
    imgsrc: '@/assets/images/metrics.png',
    title: 'Comprehensive Metrics',
    description:
      'We analyze crucial skin health indicators, ensuring our recommendations are both accurate and beneficial.',
  },
  {
    imgsrc: '@/assets/images/insurance.png',
    title: 'Upload Health Reports and Blood Work',
    description:
      'Further personalize your skincare by providing health reports and blood work, enabling our AI to consider your overall health in its analysis.',
  },
]

// Функция для получения URL-адреса изображения
const getImageUrl = path => new URL(path, import.meta.url).href
</script>

<style scoped>
.why-choose-us {
  margin-bottom: 40px;
}

.feature-list {
  list-style-type: none;
  padding: 0;
}

.feature-item {
  display: flex;
  align-items: flex-start;
  margin-bottom: 20px;
}

.feature-image {
  width: 50px; /* Установите размер изображения */
  height: auto;
  margin-right: 12px;
}

.feature-icon {
  width: 24px;
  height: 24px;
  color: var(--primary-color);
  margin-right: 12px;
  flex-shrink: 0;
}

.feature-title {
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 4px;
}

.feature-description {
  font-size: 14px;
  color: var(--text-light);
}

.background_img {
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
}
</style>
