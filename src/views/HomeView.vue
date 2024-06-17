<script setup>
import WelcomeItem from '../components/WelcomeItem.vue'
import DocumentationIcon from '../components/icons/IconDocumentation.vue'
</script>

<template>
  <main>
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Especializados en Productos de Google</template>
      Expertos certificados. Desde Google Workspace hasta Google Cloud,
      nos aseguramos de que aproveche todo el potencial de estas potentes plataformas.
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Transición Digital</template>
      Nuestro equipo de profesionales experimentados se especializa en transiciones digitales sin contratiempos. Le
      ayudamos
      a modernizar su
      infraestructura y procesos para mantenerse competitivo.
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Análisis de Datos</template>
      Tus datos son el activo más valioso. Ofrecemos servicios avanzados de análisis de datos que transforman sus datos
      en conocimientos accionables, mejorando el rendimiento general de su negocio.
    </WelcomeItem>
  </main>
</template>
