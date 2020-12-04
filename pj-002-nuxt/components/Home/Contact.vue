<template lang="pug">
v-hover(v-slot:default="{ hover }")
  v-btn.hovered(
    v-if="hover"
    retain-focus-on-click=true
    height="85px"
    width="350px"
    color="white"
    href="https://readycode.jp/contact"
    target="_brank"
  ) CONTACT
    span.hovered-mark
      font-awesome-icon(icon="comments")
  v-btn.button(
    v-else
    retain-focus-on-click=true
    shaped outlined
    color="#ffffff"
    height='80px'
    width='350px'
  ) CONTACT
    span.button-mark
      font-awesome-icon(icon="comments")
</template>

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
    padding-left: 50px;
  }
}
.hovered {
  color: red;
  font-size: 20px;
  border: 1px solid #ffffff;
  padding-top: 40px;
  text-align: center;
  font-family: 'Bebas Neue', cursive;
  letter-spacing: 1.6px;
  background-color: white;
  .hovered-mark {
    float: right;
    padding-left: 50px;
  }
}
</style>
