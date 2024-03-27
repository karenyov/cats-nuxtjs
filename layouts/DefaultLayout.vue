<!-- DefaultLayout.vue -->
<template>
  <div>
    <!-- Barra de navegação -->
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">Cats App</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    </b-navbar>

    <!-- Conteúdo principal -->
    <b-container fluid class="mt-3">
      <nuxt />
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout'
}
</script>

<style>
/* Adicione estilos personalizados aqui, se necessário */
</style>
