<template>
  <article id="resume" class="resume active" data-page="resume">
    <header>
      <h2 class="h2 article-title">
        {{ $t('pageTitles.resume') }}
      </h2>
    </header>

    <section class="timeline">
      <div class="title-wrapper">
        <div class="icon-box">
          <ion-icon name="business-outline"></ion-icon>
        </div>
        <h3 class="h3">Experience</h3>
      </div>
      <ol class="timeline-list">
        <li class="timeline-item" v-for="job in experience" :key="job.title">
          <div class="timeline-item-content">
            <!-- Item Header -->
            <div class="timeline-item-content-header">
              <!-- Title + Institution Flex Column -->
              <div class="flex-column-title">
                  <h4 class="timeline-item-title fw-bold">{{ job.title }}</h4>
                  <h6 class="timeline-item-subtitle text-light-6 text-3">
                    <ion-icon class="timeline-icon" name="business-outline"></ion-icon>
                      <span>{{ job.company }}</span>
                  </h6>
              </div>

              <div class="flex-column-date">
                  <!-- Date Tags -->
                  <div class="tag">
                    <ion-icon class="timeline-icon" name="calendar-outline"></ion-icon>
                    <span>{{ job.date}}</span>
                  </div>
              </div>
            </div>
            <div class="timeline-item-content-body mt-2">
              <p class="text-3 timeline-description">{{ job.description }}</p>
            </div>
          </div>

          <!-- Etiquetas de tecnologías -->
          <ul class="job-technologies">
            <li v-for="technology in job.technologies" :key="technology">
              {{ technology }}
            </li>
          </ul>
        </li>
      </ol>
    </section>

    <section class="timeline">
      <div class="title-wrapper">
        <div class="icon-box">
          <ion-icon name="book-outline"></ion-icon>
        </div>

        <h3 class="h3">Education</h3>
      </div>
      <ol class="timeline-list">
        <li class="timeline-item" v-for="job in education" :key="job.title">
          <div class="timeline-item-content">
            <!-- Item Header -->
            <div class="timeline-item-content-header">
              <!-- Title + Institution Flex Column -->
              <div class="flex-column-title">
                  <h4 class="timeline-item-title fw-bold">{{ job.title }}</h4>
                  <h6 class="timeline-item-subtitle text-light-6 text-3">
                    <ion-icon class="timeline-icon" name="business-outline"></ion-icon>
                      <span>{{ job.university }}</span>
                  </h6>
              </div>

              <div class="flex-column-date">
                  <!-- Date Tags -->
                  <div class="tag">
                    <ion-icon class="timeline-icon" name="calendar-outline"></ion-icon>
                    <span>{{ job.date}}</span>
                  </div>
              </div>
            </div>
          </div>  
        </li>
      </ol>
      <div class="download-button-container">
        <a
          href="https://github.com/christiantesen/christiantesen/blob/main/ChristianTesenBecerra-CV.pdf"
          aria-label="Download Resume"
          class="cta"
        >
          <span>Download Full Resume</span>
          <svg width="13px" height="10px" viewBox="0 0 13 10">
            <path d="M1,5 L11,5"></path>
            <polyline points="8 1 12 5 8 9"></polyline>
          </svg>
        </a>
      </div>
    </section>
  </article>
</template>

<script setup>
const experience = [
  {
    title: 'Software Engineer',
    date: '06/2023 ➔ 12/2023',
    company: 'AFISCA S.A.C.',
    description:'Desarrollé módulos eficientes para PDF y optimicé flujos de trabajo de Kardex. Mantuve y mejoré la red interna y bases de datos, asegurando rendimiento y estabilidad. Contribuí a la innovación tecnológica y validé soluciones con pruebas exhaustivas.',
    technologies: ['Python', 'FastAPI', 'Flutter', 'Bash', 'Windows Server','Git', 'MySQL'],
  },
  {
    title: 'Full Stack Developer (Flutter/FastAPI)',
    date: '11/2022 ➔ 05/2023',
    company: 'NEO DETER DE PERU S.A.C',
    description: 'Desarrollé aplicaciones móviles en Android con Flutter, enfocado en optimizar el rendimiento y la experiencia del usuario. Implementé microservicios en FastAPI para aplicaciones multiplataforma, mejorando la escalabilidad del sistema. Mantuve y optimicé bases de datos para asegurar integridad y rendimiento óptimo de la información, implementando medidas para garantizar la disponibilidad y consistencia de los datos críticos.',
    technologies: ['Flutter', 'Node.js', 'Dart', 'MySQL', 'Git'],
  },
  {
    title: 'IT Support and Maintenance Technician',
    date: '01/2014 ➔ 03/2014 | 01/2016 ➔ 03/2016',
    company: 'PERUPLAST S.A',
    description: 'Lideré mantenimiento preventivo de hardware para garantizar disponibilidad continua. Proporcioné soporte técnico para configuración y optimización de aplicaciones y dispositivos. Instalé y actualicé sistemas operativos y aplicaciones, asegurando seguridad y actualización constante. Implementé backups regulares y recuperación de datos para mantener integridad y disponibilidad de información crítica. Capacité a empleados en el uso efectivo de sistemas y software, mejorando eficiencia operativa y adopción tecnológica. Implementé herramientas de monitoreo para optimizar rendimiento y recursos.',
    technologies: ['Excel', 'PowertPoint', 'SQL Server', 'C#', 'Windows Server', 'VMware', 'Cisco', 'Linux', 'Git'],
  },
] 
const education = [
  {
    title: 'Ingeniería Informática',
    date: '08/2016 ➔ Actualidad',
    university: 'UNIVERISDAD RICARDO PALMA'
  }
]
</script>

<style scoped>
/* Estilos para el botón de descarga */
.download-button-container {
  margin-top: 20px;
}

a {
  text-decoration: none;
  color: inherit;
}

.cta {
  position: relative;
  display: inline-flex;
  margin: auto;
  padding: 19px 22px;
  transition: all 0.2s ease;
}

.cta:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  display: block;
  border-radius: 28px;
  background: rgba(45,212,191,.1);
  width: 46px;
  height: 46px;
  transition: all 0.3s ease;
}

.cta span {
  position: relative;
  font-size: var(--fs-8);
  line-height: 10px;
  font-weight: var(--fw-800);
  letter-spacing: 0.25em;
  text-transform: uppercase;
  vertical-align: middle;
  color: rgb(94 234 212);
}

.cta svg {
  position: relative;
  align-self: center;
  top: 0;
  margin-left: 10px;
  fill: none;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke: rgb(94 234 212);
  stroke-width: 2;
  transform: translateX(-5px);
  transition: all 0.3s ease;
}

.cta:hover:before {
  width: 100%;
  background: rgba(45,212,191,.1);
}

.cta:hover svg {
  transform: translateX(0);
}

.cta:active {
  transform: scale(0.96);
}

</style>