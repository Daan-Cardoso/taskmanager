<template>
  <div id="app">
    <CardProject name="Green House" shortName="GH" :selected="false" :template="1" />
    <CardProject name="Cyber Punk" shortName="CP" :selected="false" :template="2" />
    <CardProject name="Easy Crypto" shortName="EC" :selected="false" :template="3" />
    <CardProject name="Travel App" shortName="TA" :selected="false" :template="4" />
    <CardProject name="Landing Page" shortName="LP" :selected="false" :template="5" />
  </div>
</template>

<script>
import CardProject from './components/CardProject/CardProject'

export default {
  name: 'App',
  components: {
    CardProject
  }
}
</script>

<style>
  * {
    padding: 0;
    margin: 0;
  }
  #app {
    display: flex;
    column-gap: 10px;
    margin: 10px;
  }
</style>
