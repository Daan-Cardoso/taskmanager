<template>
  <label class="checkbox__label" :for="checkboxId">
    <i
      :class="{'checkbox--active' : active}"
      class="checkbox"
    ></i>
    <input class="checkbox-hiden" type="checkbox" v-model="active" />
    <p class="checkbox__text">{{text}}</p>
  </label>
</template>

<script>
export default {
  name: 'Checkbox',
  props: {
    text: String,
    active: Boolean
  },
  data () {
    return {
    }
  },
  methods: {
  }
}
</script>

<style lang="scss">
  @import './style.scss';
</style>
