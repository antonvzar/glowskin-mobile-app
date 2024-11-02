<template>
  <footer class="footer">
    <div class="container">
      <nav class="footer-nav">
        <a href="#" class="footer-link">For Business</a>
        <a href="#" class="footer-link">Affiliates</a>
        <a href="#" class="footer-link">Terms & Policies</a>
        <a href="#" class="footer-link">Contact us</a>
      </nav>
    </div>
    <div class="social-icons">
      <div class="social-icons">
        <FacebookIcon class="social-icon" />
        <InstagramIcon class="social-icon" />
        <TwitterIcon class="social-icon" />
      </div>
    </div>
    <div class="copyright">
      <p>&copy;2024 ProjectGlow Skin Co. All Rights Reserved.</p>
    </div>
  </footer>
</template>

<script setup>
import { FacebookIcon, InstagramIcon, TwitterIcon } from 'lucide-vue-next'
</script>

<style scoped>
.footer {
  background-color: hsl(96, 24%, 96%);
  color: #000000;
  padding: 24px 0;
}

.copyright {
  text-align: center;
  color: grey;
  margin-bottom: 16px;
  font-size: 14px;
}

.footer-nav {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 16px;
}

.footer-link {
  color: #000000;
  text-decoration: none;
  font-size: 14px;
}

.footer-link:hover {
  text-decoration: underline;
}

.social-icons {
  display: flex;
  justify-content: space-around;
  gap: 30px;
  margin-top: 15px;
  margin-bottom: 15px;
}
</style>
