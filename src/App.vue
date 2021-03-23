<template>
  <div id="app">
    <ButtonMenu/>
  </div>
</template>

<script>
import ButtonMenu from './components/ButtonMenu/ButtonMenu'

export default {
  name: 'App',
  components: {
    ButtonMenu
  }
}
</script>

<style>
  * {
    padding: 0;
    margin: 0;
  }
</style>
