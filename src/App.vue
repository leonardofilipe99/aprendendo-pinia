<template>

  <div class="app">
      <nav>
        <RouterLink to="/">Inicio</RouterLink> -

        <RouterLink to="/about">Sobre</RouterLink>
      </nav>

  <RouterView />
  </div>
</template>

<style type="text/css">
  .app {
    text-align:center;
  }
</style>