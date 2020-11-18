<template lang="pug">
v-card.list(
  color='#4593CC'
  flat
  outlined
  )
  v-hover(
    v-slot:default="{ hover }"
    v-for="item of items"
    v-bind:key="item.japanese"
    )
    v-list-item.hover(v-if="hover" :href="item.url")
      v-list-item-content
        v-list-item-line {{ item.japanese }}
    v-list-item.line(v-else)
      v-list-item-line {{ item.message }}
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        message: 'HOME',
        japanese: 'ホーム'
      },
      {
        message: 'WHO WE ARE',
        japanese: '私たちについて'
      },
      {
        message: 'WHAT WE DO',
        japanese: 'サービス・製品'
      },
      {
        message: 'NEWS',
        japanese: 'ニュース',
        url: '/news'
      },
      {
        message: 'CAREERS',
        japanese: '採用情報'
      },
      {
        message: 'OUR TEAM',
        japanese: 'メンバー'
      },
      {
        message: 'COMPANY',
        japanese: '企業情報'
      }
    ]
  })
}
</script>
<style scoped lang="scss">
.list {
  width: 392px;
  height: 552px;
  padding-top: 10%;
}

.line {
  letter-spacing: 7.2px;
  text-align: left;
  color: #ffffff;
  opacity: 1;
  font: normal 40px/80px 'Bebas Neue';
  line-height: 80px;
}
.hover {
  font-size: 18px;
  font-family: 'Hiragino Kaku Gothic Std';
}
</style>
