<template>
  <button class="buttons addTask">
      <i class="addTask__icon"></i>
    </button>
</template>

<script>
export default {
  name: 'ButtonAddTask',
  props: {
    msg: String
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
