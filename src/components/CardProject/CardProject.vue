<template>
  <div class="project">
    <div
      :class="[
                {'project__card--selected': selected || active},
                {'project__card--pink': template == 1},
                {'project__card--aqua': template == 2},
                {'project__card--purple': template == 3},
                {'project__card--blue': template == 4},
                {'project__card--orange': template == 5},
              ]"
      class="buttons project__card"
      @click="toggleCardState"
    >
      <div
        :class="[
                  {'project__shortName--pink': template == 1},
                  {'project__shortName--aqua': template == 2},
                  {'project__shortName--purple': template == 3},
                  {'project__shortName--blue': template == 4},
                  {'project__shortName--orange': template == 5},
                ]"
        class="project__shortName"
      >
          {{shortName}}
      </div>
    </div>

    <p class="project__name">{{name}}</p>
  </div>
</template>

<script>
export default {
  name: 'CardProject',
  props: {
    name: String,
    shortName: String,
    selected: Boolean,
    template: Number
  },
  data () {
    return {
      active: false
    }
  },
  methods: {
    toggleCardState () {
      this.active = !this.active
    }
  }
}
</script>

<style lang="scss">
  @import './style.scss';
</style>
