<template>
  <button @click="toggleMenuState()" class="buttons menu">
  <i
    v-bind:class="{'menu__icon--active' : this.menuOpen}"
    class="menu__icon"
  ></i>
</button>
</template>

<script>
export default {
  name: 'ButtonMenu',
  props: {
    msg: String
  },
  data () {
    return {
      menuOpen: false
    }
  },
  methods: {
    toggleMenuState () {
      this.menuOpen = !this.menuOpen
    }
  }
}
</script>

<style lang="scss">
  @import './style.scss';
</style>
