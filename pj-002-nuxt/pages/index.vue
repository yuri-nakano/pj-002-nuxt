<template lang="pug">
v-container.container(fluid)
  div.pj002
    div.picture
      div.back
        v-row
          v-col(cols="3" md="2")
            v-row.top(justify="center")
              TopMark(@click.native="overlay=false")
          v-spacer(v-if="$vuetify.breakpoint.mdAndUp")
          v-col(cols="7" v-if="$vuetify.breakpoint.smAndDown")
          v-col(cols="2" md="2" )
            v-row.menu(justify="center" )
              MenuMark(
                @toggle="overlay = !overlay"
                :overlay="overlay"
              )
        v-overlay(
          :absolute="absolute"
          :opacity="opacity"
          :color="color"
          :value="overlay"
        )
            Overlay
        v-row.continue(align="center" justify="center")
          v-spacer
          v-col(md="4" cols="8")
            v-row(justify="center")
              AlertBox
          v-spacer
        v-row.gap
        v-row(justify="end")
          v-spacer
          v-col(cols="7" md="3")
            v-row(justify="center")
              FooterLogoMark
</template>

<script>
// @ is an alias to /src
import TopMark from '@/components/TopMark.vue'
import MenuMark from '@/components/MenuMark.vue'
import Overlay from '@/components/Overlay.vue'
import AlertBox from '@/components/AlertBox.vue'
import FooterLogoMark from '@/components/FooterLogoMark.vue'
import List from '@/components/List.vue'
import MenuLine from '@/components/MenuLine.vue'
import Contact from '@/components/Contact.vue'
import BottomBtn from '@/components/BottomBtn.vue'
export default {
  name: 'Pj002',
  components: {
    TopMark,
    MenuMark,
    Overlay,
    AlertBox,
    FooterLogoMark,
    List,
    MenuLine,
    Contact,
    BottomBtn
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

.pj002 {
  margin: -11px -13px;
  .picture {
    width: 100%;
    height: 100vh;
    min-height: 100%;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    background-image: url('../assets/background.png');
    .back {
      height: auto;
      margin-bottom: 0px;
      height: 100vh;
      max-width: 100%;
      background: 0% 0% cover padding-box;
      background-color: rgba(0, 0, 0, 0.85);
    }
  }
  .top {
    z-index: 100;
    margin-left: 30%;
  }
  .menu {
    z-index: 200;
    margin-right: 45%;
  }
  .wolf {
    float: left;
    width: 110px;
    height: 130px;
  }
  .continue {
    height: 60%;
  }
  .gap {
    height: 10%;
  }
  .v-overlay__content {
    margin: 0%;
    padding: 0%;
    width: 100vw;
    height: 100vh;
  }
}
</style>
