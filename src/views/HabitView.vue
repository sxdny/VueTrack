<script setup lang="ts">
import { ref } from 'vue'

/*
Recordar que hay dos tipos de importaciones:
- import { ref } from 'vue'; <-- Esta importa una función
- import ref from 'vue'; <-- Esta importa un objeto
*/

import HabitView from '../components/HabitView.vue'

interface Habit {
  id: number,
  name: string
  description: string
  counter: number
  streaks: number
  type: string
}

let habits: Array<Habit> = ref([
  {
    id: 1, // Importante: No olvidar el id SIEMPRE
    name: 'Ejercicio',
    description: 'Hacer ejercicio por 30 minutos',
    counter: 0,
    streaks: 0,
    type: 'daily'
  },
  {
    id: 2,
    name: 'Leer',
    description: 'Leer 20 páginas de un libro',
    counter: 0,
    streaks: 0,
    type: 'daily'
  },
  {
    id: 3,
    name: 'Meditar',
    description: 'Meditar por 10 minutos',
    counter: 0,
    streaks: 0,
    type: 'daily'
  },
  {
    id: 4,
    name: 'Programar',
    description: 'Programar por 1 hora',
    counter: 0,
    streaks: 0,
    type: 'daily'
  },
  {
    id: 5,
    name: 'Escribir',
    description: 'Escribir por 30 minutos',
    counter: 0,
    streaks: 0,
    type: 'daily'
  }
])

function handleCreateHabit() {
  // Primero hacemos el form digamos de crear el hábito
}

const createHabitDialog = document.getElementById('createHabitDialog');

const openCreateHabitDialog = () => {
  console.log('Abrir diálogo para crear hábito');
  createHabitDialog?.showModal()
}
</script>

<template>
  <main>
    <header>
      <h1>Página para crear hábitos</h1>
      <p>En esta página podrás crear hábitos y ver tu progreso.</p>
    </header>
    <div class="actions">
      <button @click="openCreateHabitDialog">Crear hábito +</button>
    </div>
    <div class="habits">
      <div v-for="habit in habits">
        <HabitView :habit="habit" />
      </div>
    </div>
  </main>

  <dialog id="createHabitDialog">
      <h2>Diálogo para crear un hábito</h2>
      <p>Crear un hábito</p>
  </dialog>

</template>

<style scoped>

main {
  padding: 1rem;
}

header > p {
  font-size: 1.25rem;
  color: #727272;
}

.actions {
  display: flex;
  justify-content: flex-start;
  padding: 1rem 0;
  gap: 1rem;
}

.habits {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

#createHabitDialog[open] {
  background-color: red;
  position: fixed;
  width: 50%;
  height: 50%;
  top: 50%;
  left: 50%;
}

#handleNewHabit {
  padding: 1rem;
  background-color: #000000;
  border: 0.5px solid #727272;
  color: #fff;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

#handleNewHabit:hover {
  background-color: #313131;
}
</style>
