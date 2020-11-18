<template lang="pug">
  .alert(@click="alert()")
    v-btn.button(outlined color="white" tile height='80px' width='278px') continue
      span.button-mark
        font-awesome-icon(icon="chevron-right")
</template>
<script>
export default {
  data() {
    return {
      message: 'コンティニューボタンが押されました'
    }
  },
  methods: {
    alert() {
      window.alert(this.message)
    }
  }
}
</script>

<style scoped lang="scss">
.button {
  color: #ffffff;
  font-size: 20px;
  border: 1px solid #ffffff;
  padding-top: 40px;
  // position: absolute;
  text-align: center;
  font-family: 'Bebas Neue', cursive;
  letter-spacing: 1.6px;
  .button-mark {
    color: #ffffff;
    float: right;
    padding-left: 40px;
  }
}
</style>
