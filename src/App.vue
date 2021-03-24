<template>
  <div id="app">
    <Checkbox text="Input your text here"/>
    <Checkbox text="teste 2"/>
    <Checkbox text="dash"/>
    <Checkbox text="drift drift drift" :active="true"/>
  </div>
</template>

<script>
import Checkbox from './components/Checkbox/Checkbox'

export default {
  name: 'App',
  components: {
    Checkbox
  }
}
</script>

<style>
  * {
    padding: 0;
    margin: 0;
  }
</style>
