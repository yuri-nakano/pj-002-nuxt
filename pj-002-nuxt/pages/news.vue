<template lang="pug">
v-container.container(fluid)
  div.page
    v-row.newstop
      v-col.top(cols="3" md="2")
        v-row(justify="center")
          TopMark(
            link nuxt to="/"
            style="z-index:2000;position: fixed;"
          )
          LeftSquare
      v-spacer(v-if="$vuetify.breakpoint.mdAndUp")
      v-col(cols="7" v-if="$vuetify.breakpoint.smAndDown")
      v-col(cols="2" md="2" )
        v-row.menu(justify="center")
          MenuMark(
            @toggle="overlay = !overlay"
            :overlay="overlay"
            style="z-index:3000;position: fixed;"
          )
      v-overlay(
        style="z-index:1000"
        :absolute="absolute"
        :opacity="opacity"
        :color="color"
        :value="overlay"
      )
        Overlay
    v-row.heder
      v-col.back(md='12')
        v-row
          div.backcolor
          div.newslogo(style="z-index:200;position:absolute;")
            NewsLetter
      v-spacer
      v-col.btn(md='6')
        v-row
          NewsList
    v-row.footerbottom
    v-row
      v-col(md='12')
        v-row
          NewsFooter

</template>
<script>
import NewsLetter from '@/components/News/NewsLetter.vue'
import TopMark from '@/components/Home/TopMark.vue'
import MenuMark from '@/components/Home/MenuMark.vue'
import Overlay from '@/components/Home/Overlay.vue'
import LeftSquare from '@/components/News/LeftSquare.vue'
import NewsList from '@/components/News/NewsList.vue'
import NewsFooter from '@/components/News/NewsFooter.vue'
export default {
  components: {
    NewsLetter,
    TopMark,
    MenuMark,
    Overlay,
    LeftSquare,
    NewsList,
    NewsFooter
  },
  data: () => ({
    overlay: false,
    absolute: true,
    color: '#4593CC',
    opacity: 1.0
  })
}
</script>
<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');
.container {
  margin: 0;
  padding: 0px;
  .footerbottom {
    height: 7%;
  }
  .page {
    background-color: white;
    width: 100%;
    height: 400vh;
    .top {
      padding: 0;
    }
    .lists {
      top: -50%;
    }
    .topbtn {
      top: -10px;
    }
  }
  .newslogo {
    height: 100px;
    background-image: url('../assets/newslogo.png');
    width: 100vw;
    top: 18%;
    background-size: cover;
  }
  .backcolor {
    background-color: #f8f8f8;
    height: 300px;
    width: 100%;
    position: relative;
    z-index: 0;
  }
  .btn {
    padding: 0%;
    margin-top: -80px;
    z-index: 100;
  }
}
.back {
  padding: 0%;
}
.newstop {
  height: 20%;
}
</style>
