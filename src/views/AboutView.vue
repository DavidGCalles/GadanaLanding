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
      Ofrecer soluciones tecnológicas innovadoras y personalizadas que impulsen la eficiencia,
      mejoren la productividad y desbloqueen nuevas oportunidades de crecimiento. Creemos en el poder de la tecnología
      para transformar negocios y estamos comprometidos a guiarlo en cada paso de su viaje digital.
    </WelcomeItem>
    
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Los procesos de las grandes empresas, en tu casa</template>
      Provenientes de los entornos corporativos más sólidos, nuestro equipo de consultores aplicará la ingeniería
      de datos y software más exigente para proveer a nuestros clientes de una ventaja competitiva usualmente poco
      accesible.
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Soluciones Integrales</template>
      Maximice la eficiencia y reduzca errores automatizando sus procesos empresariales. En Gadana Solutions, diseñamos
      y ejecutamos soluciones de automatización personalizadas que optimizan sus operaciones, ahorrándole tiempo y
      recursos valiosos.
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