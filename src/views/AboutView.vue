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
      <template #heading>Nuestra Misión</template>
      Nuestra misión es ofrecer soluciones tecnológicas innovadoras y personalizadas que impulsen la eficiencia,
      mejoren la productividad y desbloqueen nuevas oportunidades de crecimiento. Creemos en el poder de la tecnología
      para transformar negocios y estamos comprometidos a guiarlo en cada paso de su viaje digital.
    </WelcomeItem>
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Experiencia en Productos de Google</template>
      Como expertos certificados en productos de Google, proporcionamos soluciones integrales para integrar y
      optimizar la suite de herramientas de Google en su empresa. Desde Google Workspace hasta Google Cloud,
      nos aseguramos de que aproveche todo el potencial de estas potentes plataformas.
    </WelcomeItem>
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Transición Digital</template>
      Navegar por el panorama digital puede ser un desafío. Nuestro equipo de profesionales experimentados se
      especializa en transiciones digitales sin contratiempos, asegurando que su negocio se adapte a nuevas tecnologías
      con
      mínima
      interrupción. Le ayudamos a modernizar su infraestructura y procesos para mantenerse competitivo.
    </WelcomeItem>
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Automatización de Procesos</template>
      Maximice la eficiencia y reduzca errores automatizando sus procesos empresariales. En Gadana Solutions, diseñamos
      y ejecutamos soluciones de automatización personalizadas que optimizan sus operaciones, ahorrándole tiempo y
      recursos valiosos.
    </WelcomeItem>
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Análisis de Datos</template>
      En la era de la información, los datos son el activo más valioso. Ofrecemos servicios avanzados de análisis de
      datos
      que transforman sus datos en conocimientos accionables, impulsando decisiones estratégicas y mejorando el
      rendimiento general de su negocio.
    </WelcomeItem>




  </main>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>