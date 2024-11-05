<template>
  <div class="app">
    <Header />
    <main class="container">
      <HeroSection />
      <SystemDescription />
      <SuggestionSection />
      <WhyChooseUs />
      <AnalysisSteps />
      <CommunitySection />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import SuggestionSection from './components/SuggestionSection.vue'
import AnalysisSteps from './components/AnalysisSteps.vue'
import CommunitySection from './components/CommunitySection.vue'
import Footer from './components/Footer.vue'
import SystemDescription from './components/SystemDescription.vue'
import WhyChooseUs from './components/WhyChooseUs.vue'
</script>

<style>
@import './assets/global.css';

@media screen and (max-width: 768px) {
  .app {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  main {
    flex: 1;
    padding-top: 20px;
    padding-bottom: 20px;
  }

  .container {
    padding: 0 15px;
  }
}

@media screen and (min-width: 769px) {
  .container {
    margin: 0 auto;
  }
}
</style>
