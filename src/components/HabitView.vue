<script setup lang="ts">
/*
Hay dos formas de definir props, pero como estamos
usando lang="ts" en el script setup, usaremos este método
*/

const props = defineProps({
  habit: {
    type: Object,
    required: true
  }
})

// Funciones del compontente
const handleIncrementCounter = () => {
  props.habit.counter++
  console.log(
    'Contador incrementado del botón:',
    props.habit.id,
    'Valor del contador: ',
    props.habit.counter
  )
}

const handleResetCounter = () => {
  props.habit.counter = 0
  console.log(
    'Contador reiniciado del botón:',
    props.habit.id,
    'Valor del contador: ',
    props.habit.counter
  )
}

</script>

<template>
  <div class="habit">
    <header>
      <h2>{{ habit.name }}</h2>
      <p>{{ habit.description }}</p>
    </header>
    <div class="habitInfo">
      <h3>Información sobre el hábito:</h3>
      <ul>
        <li>
          Contador:
          <span>
            {{ habit.counter === 0 ? 'No has iniciado este hábito' : `${habit.counter}` }}
          </span>
        </li>
        <li>Racha: {{ habit.streaks }}</li>
        <li>Tipo: {{ habit.type }}</li>
      </ul>
    </div>
    <div class="actions">
      <button @click="handleIncrementCounter">Incrementar contador</button>
      <button @click="handleResetCounter">Reiniciar contador</button>
    </div>
  </div>
</template>

<style scoped>
/* Aqui va los estilos de nuestro componente. */
.habit {
  background-color: #222;
  border: 1px solid #727272;
  border-radius: 10px;
  width: 20rem;
}

button {
  padding: 0.5rem 1rem;
  background-color: #000000;
  border: 0.5px solid #727272;
  color: #fff;
  border-radius: 5px;
  cursor: pointer
}

button:hover {
  background-color: #222;
  transition: .25s ease;
}

.actions {
  display: flex;
  justify-content: space-around;
  padding: 1rem;
  gap: .5rem
}

.habitInfo {
  padding: 1rem;
}

.habitInfo > h3 {
  font-size: 14px;
  color: #b9b9b9;
}

.habitInfo > ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.habitInfo > ul > li {
  padding: 0.5rem 0;
  color: rgb(145, 255, 0);
}

header {
  display: flex;
  flex-direction: column;
  background-color: rgb(17, 17, 17);
  padding: 1rem;
  border-radius: 10px 10px 0 0;
}
h2 {
  color: rgb(145, 255, 0);
  font-weight: bold;
}
</style>
