<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    
    <div class="wrapper">
    
      <nav>
        <ul>
          <li>
            <RouterLink to="/">Home</RouterLink>
          </li>
          <li>
            <RouterLink to="/about">About</RouterLink>
          </li>
        </ul>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<!-- El scoped solo aplica los estilos a los
elementos de este componente -->
<style scoped>

nav > ul {
  display: flex;
  gap: 1rem;
  padding: 1rem;
  background-color: white;
  list-style: none;
  text-decoration: none;
}

li > a {
  text-decoration: none;
  color: black;
}

li > a:hover {
  color: #727272;
}

</style>

