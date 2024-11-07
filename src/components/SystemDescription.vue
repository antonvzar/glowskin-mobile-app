<template>
  <section class="why-choose-us">
    <div class="content">
      <!-- Desktop version content -->
      <div v-if="isDesktop" class="text-content">
        <h2 class="section-title">A New Era of Skincare</h2>
        <p class="features-description">
          Go beyond traditional surface-level assessments with personalized
          solutions that cater to every aspect of your skin's needs. Embrace a
          new era of skincare, precisely tailored to your unique biological
          blueprint and lifestyle.
        </p>

        <h3 class="section-subtitle">
          The Most Comprehensive Skin Health Analysis
        </h3>

        <ul class="feature-list main-features">
          <li
            v-for="(feature, index) in features.slice(0, 4)"
            :key="index"
            class="feature-item"
          >
            <img
              :src="feature.imgsrc"
              alt="Feature Image"
              class="feature-image"
            />
            <div>
              <h3 class="feature-title" style="font-weight: bold">
                {{ feature.title }}
              </h3>
              <p class="feature-description">{{ feature.description }}</p>
            </div>
          </li>
        </ul>
      </div>

      <!-- Desktop additional features on the right -->
      <div v-if="isDesktop" class="img-container">
        <img
          class="background_img"
          src="@/assets/images/ai-girl.svg"
          alt="AI Girl Image"
        />
        <ul class="feature-list extra-features">
          <li
            v-for="(feature, index) in features.slice(4)"
            :key="index + 4"
            class="feature-item"
          >
            <img
              :src="feature.imgsrc"
              alt="Feature Image"
              class="feature-image"
            />
            <div>
              <h3 class="feature-title" style="font-weight: bold">
                {{ feature.title }}
              </h3>
              <p class="feature-description">{{ feature.description }}</p>
            </div>
          </li>
        </ul>
      </div>

      <!-- Mobile version content -->
      <div v-else>
        <div class="img-container">
          <img
            class="background_img"
            src="@/assets/images/ai-girl.svg"
            alt="AI Girl Image"
          />
        </div>
        <div class="text-content">
          <h2 class="section-title">A New Era of Skincare</h2>
          <p class="features-description">
            Go beyond traditional surface-level assessments with personalized
            solutions that cater to every aspect of your skin's needs. Embrace a
            new era of skincare, precisely tailored to your unique biological
            blueprint and lifestyle.
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
                :src="feature.imgsrc"
                alt="Feature Image"
                class="feature-image"
              />
              <div>
                <h3 class="feature-title" style="font-weight: bold">
                  {{ feature.title }}
                </h3>
                <p class="feature-description">{{ feature.description }}</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import analysingImg from '@/assets/images/analysing.svg'
import faceRecognitionImg from '@/assets/images/face-recognition.svg'
import profileImg from '@/assets/images/profile.svg'
import dnaImg from '@/assets/images/dna.svg'
import metricsImg from '@/assets/images/metrics.svg'
import insuranceImg from '@/assets/images/insurance.svg'

const features = [
  {
    imgsrc: analysingImg,
    title: 'Extensively Trained',
    description:
      'Our technology has been trained on a diverse dataset of 100,000+ images to ensure high accuracy and reliability.',
  },
  {
    imgsrc: faceRecognitionImg,
    title: 'Image Recognition and Analysis',
    description:
      'Simply upload a selfie and our AI will instantly begin its detailed assessment, identifying and addressing key areas of concern with remarkable accuracy.',
  },
  {
    imgsrc: profileImg,
    title: 'Personalised Recommendations',
    description:
      "Sophisticated algorithms deliver precise product suggestions tailored to your skin's specific needs.",
  },
  {
    imgsrc: dnaImg,
    title: 'Upload DNA Report',
    description:
      'Integrate genetic insights by uploading your DNA report, allowing us to refine your skincare recommendations based on your genetic predispositions.',
  },
  {
    imgsrc: metricsImg,
    title: 'Comprehensive Metrics',
    description:
      'We analyze crucial skin health indicators, ensuring our recommendations are both accurate and beneficial.',
  },
  {
    imgsrc: insuranceImg,
    title: 'Upload Health Reports and Blood Work',
    description:
      'Further personalize your skincare by providing health reports and blood work, enabling our AI to consider your overall health in its analysis.',
  },
]

// Detect if the device is a desktop
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
/* Общие стили */
.why-choose-us {
  margin-bottom: 40px;
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* Remove bullets and align items horizontally */
.feature-list {
  list-style-type: none;
  padding: 0;
}

.feature-item {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}

.feature-image {
  width: 50px;
  height: auto;
  margin-right: 12px;
}

/* Мобильные стили */
@media screen and (max-width: 900px) {
  .background_img {
    width: 90vw;
    height: 75.56vw;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  .feature-item {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
  }
}

/* Десктопные стили */
@media screen and (min-width: 901px) {
  .content {
    flex-direction: row;
    align-items: flex-start;
    justify-content: space-between;
  }

  .text-content {
    width: 50%;
    padding-right: 20px;
  }

  .img-container {
    width: 40%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .background_img {
    width: 100%;
    height: auto;
    margin-bottom: 20px;
  }

  .main-features {
    margin-bottom: 20px;
  }

  .extra-features {
    margin-top: 20px;
  }
}
</style>
