<script setup>
import { ref } from 'vue'

const contactMethod = ref('');

const handleSubmit = (event) => {
  const formNode = document.getElementById(event.target.id)
  console.log(formNode)
  let formData = new FormData(formNode)
  console.log(formData)
  console.log("Enviando formulario de contacto")
  for (const [key, value] of formData) {
    console.log(`${key}: ${value}\n`)
  }
  // Bootstrap validation
  if (!formNode.checkValidity()) {
    event.stopPropagation();
  } else {
    // Submit the form programmatically if validation passes
    //formNode.submit(); We comment this because we are not sending anywhere the form yet
  }

  formNode.classList.add('was-validated');
}

</script>
<template>
  <main>
    <p>Si necesitas hablar con nosotros, recibir presupuestos o hacer una consulta personal, no dudes en rellenar el
      formulario.</p>
    <form id="contactoForm" class="card needs-validation" @submit="handleSubmit">
      <div class="card-header">
        <h1 class="card-title">Contáctanos</h1>
      </div>
      <div class="card-body">
        <label class="form-label" for="contactSelected">Elige tu medio de comunicación para la respuesta:</label>
        <select class="form-select" id="contactSelected" name="contactSelected" v-model="contactMethod" required>
          <option value="telefono">Telefono</option>
          <option value="email" selected>Correo Electrónico</option>
          <option value="Red Social" disabled>Red social</option>
        </select>
        <br>
        <div v-if="contactMethod == 'email'">
          <label class="form-label" for="senderEmail">Correo Electrónico: </label>
          <input class="form-control" id="senderEmail" name="senderEmail" type="email" required>
        </div>
        <div v-if="contactMethod == 'telefono'">
          <label class="form-label" for="senderPhone">Teléfono: </label>
          <input class="form-control" id="senderPhone" name="senderPhone" type="tel" required>
        </div>
        <br>
        <label class="form-label" for="topic">Tema de contacto: </label>
        <select class="form-select" id="topic" name="topic" required>
          <option value="Google Apps Script">Google Apps Script</option>
          <option value="Google Workspace">Google Workspace</option>
          <option value="Google Cloud Platform">Google Cloud Platform</option>
          <option value="Otros desarrollos">Otros desarrollos</option>
        </select>
        <br>
        <label class="form-label" for="motivoConsulta">Motivo de la consulta: </label>
        <textarea class="form-control" id="motivoConsulta" name="motivoConsulta" required>
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
