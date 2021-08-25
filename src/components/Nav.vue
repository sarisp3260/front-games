<template>
  <div class="nav__menu">
    <a>¿Qienes Somos?</a>
    <a>Registrarse</a>
  </div>
  <Button title="Iniciar Sesión" class="regular"/>
</template>

<script>
import Button from './Button.vue'

export default {
  name: 'Nav',
  components: { Button },
}
</script>

<style>
.nav__menu {
  align-items: center;
  margin-left: auto;
  margin-right: 20px;
  display: flex;
  height: 65px;
  padding: 0 50px;
}
.nav__menu a {
  color: var(--secundary-color);
  padding: 0 12px;
  display: flex;
  text-decoration: none;
  cursor: pointer;
  font-size: var(--size);
}
</style>