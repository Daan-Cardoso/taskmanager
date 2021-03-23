<template>
  <div class="search">
    <i @mouseover.stop
      :class="{'icon-search--hide': searchFocus}"
      class="icon icon-search"
    ></i>
    <i
      class="icon icon-typing"
      :class="[
                {'icon-typing--hide': !searchFocus},
                {'icon-typing--animate': typingIcon}
              ]"
    ></i>
    <input
      type="text"
      class="search__input"
      placeholder="Search Task or Project"
      @keyup="toggleTypingAnimate"
      @focus="toggleSearchFocus"
      @blur="toggleSearchFocus"
    >
  </div>
</template>

<script>
export default {
  name: 'SearchInput',
  props: {
    msg: String
  },
  data () {
    return {
      searchFocus: false,
      typingIcon: false
    }
  },
  methods: {
    toggleSearchFocus () {
      this.searchFocus = !this.searchFocus
    },
    toggleTypingAnimate ($event) {
      const typing = $event.target.value.length > 0
      typing ? this.typingIcon = true : this.typingIcon = false
    }
  }
}
</script>

<style lang="scss">
  @import './style.scss';
</style>
