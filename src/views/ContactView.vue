<script setup>
import { ref } from 'vue'

const contactMethod = ref('');

</script>
<template>
  <main>
    <p>Si necesitas hablar con nosotros, recibir presupuestos o hacer una consulta personal, no dudes en rellenar el
      formulario.</p>
    <form class="card needs-validation">
      <div class="card-header"><h1 class="card-title">Contáctanos</h1></div>
      <div class="card-body">
      <label class="form-label" for="contactSelected">Elige tu medio de comunicación para la respuesta:</label>
      <select class="form-select" id="contactSelected" v-model="contactMethod">
        <option value="telefono">Telefono</option>
        <option value="email">Correo Electrónico</option>
        <option value="Red Social" disabled>Red social</option>
      </select>
      <br>
      <div v-if="contactMethod == 'email'">
        <label class="form-label" for="senderEmail">Correo Electrónico: </label>
        <input class="form-control" id="senderEmail" type="email">
      </div>
      <div v-if="contactMethod == 'telefono'">
        <label class="form-label" for="senderPhone">Teléfono: </label>
        <input class="form-control" id="senderPhone" type="tel">
      </div>
      <br>
      <label class="form-label" for="topic" name="topic">Tema de contacto: </label>
      <select class="form-select" id="topic">
        <option value="Google Apps Script">Google Apps Script</option>
        <option value="Google Workspace">Google Workspace</option>
        <option value="Google Cloud Platform">Google Cloud Platform</option>
        <option value="Otros desarrollos">Otros desarrollos</option>
      </select>
      <br>
      <label class="form-label" for="motivoConsulta">Motivo de la consulta: </label>
      <textarea class="form-control" id="motivoConsulta">
      </textarea>
      <br>
      <button type="submit" class="btn btn-primary">Enviar consulta</button>
    </div>
    </form>
  </main>
</template>

<style>

.section>div {
  display: inline;
}

.section>label {
  margin-right: 1rem;
}
</style>
