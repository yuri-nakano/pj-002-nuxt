<template lang="pug">
v-card.list(
  color='#4593CC'
  flat
  outlined
  )
    v-list-item-content(
      v-for="item of items"
      v-bind:key="item.message"
    )
      v-list-item-content
        v-list-item-line.line {{ item.message }}
          nobr.japanese  {{ item.japanese }}
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        message: 'HOME',
        japanese: 'ホーム',
        url: '/'
      },
      {
        message: 'WHO WE ARE',
        japanese: '私たちについて',
        url: ''
      },
      {
        message: 'WHAT WE DO',
        japanese: 'サービス・製品',
        url: ''
      },
      {
        message: 'NEWS',
        japanese: 'ニュース',
        url: '/news'
      },
      {
        message: 'CAREERS',
        japanese: '採用情報',
        url: ''
      },
      {
        message: 'OUR TEAM',
        japanese: 'メンバー',
        url: ''
      },
      {
        message: 'COMPANY',
        japanese: '企業情報',
        url: ''
      }
    ]
  })
}
</script>
<style scoped lang="scss">
.list {
  width: 500px;
  height: 50%;
  padding-top: 30%;
}

.line {
  letter-spacing: 7.2px;
  text-align: left;
  color: #ffffff;
  opacity: 1;
  font: normal 25px/40px 'Bebas Neue';
  line-height: 15px;
}
.japanese {
  font-size: 10px;
  font-family: 'Hiragino Kaku Gothic Std';
}
.hover {
  font: normal 25px/40px 'Bebas Neue';
}
</style>
