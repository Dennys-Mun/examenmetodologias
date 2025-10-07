<template>
  <div class="form-container">
    <h2>Registro de Usuario</h2>
    <form @submit.prevent="submit">
      <div class="form-group">
        <label>Nombre</label>
        <input v-model="name" placeholder="Escribe tu nombre" />
      </div>

      <div class="form-group">
        <label>Dirección</label>
        <input v-model="address" placeholder="Escribe tu dirección" />
      </div>

      <div class="form-group">
        <label>Edad</label>
        <input v-model.number="age" type="number" placeholder="Tu edad" />
      </div>

      <button type="submit">Guardar</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('')
const address = ref('')
const age = ref(null)

function submit() {
  alert(`Usuario registrado: ${name.value}`)
}
</script>

<style scoped>
.form-container {
  width: 320px;
  margin: 50px auto;
  padding: 20px;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
  background-color: #f9f9f9;
  font-family: Arial, sans-serif;
}

h2 {
  text-align: center;
  color: #333;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  font-weight: bold;
  margin-bottom: 5px;
  color: #444;
}

input {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 6px;
}

button {
  width: 100%;
  background-color: #2c7be5;
  color: white;
  border: none;
  padding: 10px;
  border-radius: 6px;
  cursor: pointer;
  font-weight: bold;
}

button:hover {
  background-color: #1a5ec8;
}
</style>
