<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-logo">
        <img
          src="@/assets/images/GP-logo-Skin.png"
          alt="Project Glow Skin Logo"
        />
      </div>

      <nav class="footer-nav">
        <a href="#" class="footer-link">For Business</a>
        <a href="#" class="footer-link">Affiliates</a>
        <a href="#" class="footer-link">Terms & Policies</a>
        <a href="#" class="footer-link">Contact us</a>
      </nav>

      <div class="social-icons">
        <img src="@/assets/images/facebook.png" class="social-icon" />
        <img src="@/assets/images/instagram.png" class="social-icon" />
        <img src="@/assets/images/x.png" class="social-icon" />
        <img src="@/assets/images/tik_tok.png" class="social-icon" />
      </div>

      <div class="copyright">
        <p>&copy;2024 Project Glow Skin Co. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script setup></script>

<style scoped>
.footer {
  background-color: hsl(96, 24%, 96%);
  color: #000000;
  padding: 24px 0;
  position: relative;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  margin-bottom: 50px;
}

/* Логотип */
.footer-logo {
  position: absolute;
  top: 0px;
  left: 40px;
}

.footer-logo img {
  width: 150px;
  position: absolute;
  top: 0px;
}

/* Навигация */
.footer-nav {
  display: flex;
  gap: 16px;
  position: absolute;
  top: 0px;
  right: 40px;
}

.footer-link {
  color: #000000;
  text-decoration: none;
  font-size: 14px;
}

.footer-link:hover {
  text-decoration: underline;
}

/* Социальные иконки */
.social-icons {
  display: flex;
  gap: 20px;
  position: absolute;
  top: 70px;
  right: 40px;
}

.social-icon {
  width: 24px;
  height: 24px;
}

/* Авторские права */
.copyright {
  position: absolute;
  top: 75px;
  left: 40px;
  color: grey;
  font-size: 14px;
  text-align: left;
}

/* Стили для мобильной версии */
@media screen and (max-width: 900px) {
  .container {
    flex-direction: column;
    align-items: center;
  }

  .footer-logo {
    position: static;
    margin-bottom: 16px;
  }

  .footer-nav {
    position: static;
    flex-direction: column;
    align-items: center;
    margin-bottom: 16px;
  }

  .footer-link {
    margin-bottom: 8px;
  }

  .social-icons {
    position: fixed;
    bottom: 0px;
    justify-content: center;
    gap: 20px;
    margin: 16px 0;
  }

  .copyright {
    position: static;
    text-align: center;
    margin-top: 16px;
  }
}
</style>
