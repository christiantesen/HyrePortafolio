<script setup>
let isOpen = ref(false)

function toggleMenu() {
  isOpen = !isOpen
}
</script>

<template>
  <aside class="sidebar" :class="{ active: isOpen }">
    <div class="sidebar-info">
      <figure class="avatar-box">
        <img src="/images/avatar.png" alt="Photo" width="80">
      </figure>

      <div class="info-content">
        <h1 class="name" title="Christián Tesén">
          Christián Tesén Becerra
        </h1>

        <p class="title text-center xl:block flex items-center justify-center gap-1">
          <span class="xl:after:content-[''] after:content-[',']">Software Engineer</span>
          <span>Back End Developer</span>
        </p>
      </div>

      <button class="info_more-btn" @click="isOpen = !isOpen">
        <span>Mostrar</span>

        <ion-icon name="chevron-down" />
      </button>
    </div>

    <div class="sidebar-info_more">
      <div class="separator" />

      <ul class="contacts-list">
        <a href="mailto:ctesenb@gmail.com" class="contact-item">
          <div class="icon-box">
            <ion-icon name="mail-outline"></ion-icon>
          </div>
          <div class="contact-info">
            <p class="contact-title">Correo</p>
            <span class="contact-link">ctesenb@gmail.com</span>
          </div>
        </a>

        <!-- Phone -->
        <a href="tel:+51957308626" class="contact-item">
          <div class="icon-box">
            <ion-icon name="phone-portrait-outline"></ion-icon>
          </div>
          <div class="contact-info">
            <p class="contact-title">Celular</p>
            <span class="contact-link">957 308 626</span>
          </div>
        </a>

        <!-- Linkedin -->
        <a href="https://www.linkedin.com/in/christian-tesen-becerra/" class="contact-item" target="_blank">
          <div class="icon-box">
            <ion-icon name="logo-linkedin" />
          </div>
          <div class="contact-info">
            <p class="contact-title">LinkedIn</p>
            <span class="contact-link">Christián Tesén Becerra</span>
          </div>
        </a>

        <li class="contact-item">
          <div class="icon-box">
            <ion-icon name="location-outline" />
          </div>

          <div class="contact-info">
            <p class="contact-title">
              Nacionalidad
            </p>

            <address>Perú</address>
          </div>
        </li>
      </ul>

      <div class="separator" />

      <ul class="social-list">
        
      </ul>
    </div>
  </aside>
</template>
<style scoped>

.contacts-list .contact-item:hover {
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
}

/* Estilos adicionales para el enlace del cursor */
.contacts-list .contact-item:hover .contact-link {
  text-decoration: underline;
  text-decoration-color: var(--color-secondary-3);
}

</style>
