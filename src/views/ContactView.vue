<script setup>
import { ref } from 'vue'

const contactMethod = ref('');

</script>
<template>
  <main>
    <h1>Contáctanos</h1>
    <p>Si necesitas hablar con nosotros, recibir presupuestos o hacer una consulta personal, no dudes en rellenar el
      formulario.</p>
    <form class="section">
      <label for="contactSelected">Elige tu medio de comunicación para la respuesta:</label>
      <select id="contactSelected" v-model="contactMethod">
        <option value="telefono">Telefono</option>
        <option value="email">Correo Electrónico</option>
        <option value="Red Social" disabled>Red social</option>
      </select>
      <br>
      <div v-if="contactMethod == 'email'">
        <label for="senderEmail">Correo Electrónico: </label>
        <input id="senderEmail" type="email">
      </div>
      <div v-if="contactMethod == 'telefono'">
        <label for="senderPhone">Teléfono: </label>
        <input id="senderPhone" type="tel">
      </div>
      <br>
      <label for="topic" name="topic">Tema de contacto: </label>
      <select id="topic">
        <option value="Google Apps Script">Google Apps Script</option>
        <option value="Google Workspace">Google Workspace</option>
        <option value="Google Cloud Platform">Google Cloud Platform</option>
        <option value="Otros desarrollos">Otros desarrollos</option>
      </select>
      <br>
      <label for="motivoConsulta">Motivo de la consulta: </label>
      <textarea id="motivoConsulta">
      </textarea>
      <br>
      <button type="submit">Enviar consulta</button>
    </form>
  </main>
</template>

<style>
.section {
  border: 1px solid red;
  padding: 2rem;
}
.section > div {
  display: inline;
}
.section > label{
  margin-right: 1rem;
}
</style>
