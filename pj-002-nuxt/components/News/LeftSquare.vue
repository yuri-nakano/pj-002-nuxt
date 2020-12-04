<template lang="pug">
span
  .square
    a(href="https://twitter.com/kikilala_sanrio")
      .fab.fa-twitter
    a(href="https://ja-jp.facebook.com/")
      .fab.fa-facebook
</template>
<style scoped lang="scss">
span {
  padding-top: 0px;
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 1300px 230px 0 0;
  border-color: #4593cc transparent transparent transparent;
  position: relative;
  z-index: 500;
  .square {
    top: -700px;
    height: 0;
    width: 123px;
    border-top: 50px solid #146098;
    border-right: 9px solid transparent;
    position: relative;
    z-index: 600;
  }
  .fab.fa-twitter {
    top: -55px;
    padding: 10px;
    left: 15px;
    color: #ffffff;
    font-size: 30px;
    position: relative;
    z-index: 650;
  }
  .fab.fa-facebook {
    top: -55px;
    left: 15px;
    padding: 15px;
    color: #ffffff;
    font-size: 30px;
    position: relative;
    z-index: 650;
  }
}
</style>
