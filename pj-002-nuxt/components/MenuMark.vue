<template lang="pug">
div.menu#app
  v-btn(
    @click="toggleSwitch()"
    color='white'
    width= '78px'
    height='78px'
    dark
    fab
    )
    .v-icon(v-if="overlay")
      font-awesome-icon.fa-times(icon="times" size="2x")
    .v-icon(v-else)
      font-awesome-icon.fa-bars(icon="bars" size="2x")
</template>
<script>
export default {
  props: ['overlay'],
  methods: {
    toggleSwitch() {
      this.$emit('toggle')
    }
  }
}
</script>

<style scoped lang="scss">
.menu {
  width: 78px;
  height: 78px;
  background-color: white;
  border-radius: 50%;
  margin-right: 2%;
}
.fa-bars {
  color: #4492cb;
  margin-top: 5px;
}
.fa-times {
  color: #4492cb;
  margin-top: 8px;
}
</style>
