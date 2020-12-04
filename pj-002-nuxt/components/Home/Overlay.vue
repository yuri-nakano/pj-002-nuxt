<template lang="pug">
.v-overlay__content
  v-col.main
    v-row.center(align="center")
      v-col(md="2" v-if="$vuetify.breakpoint.mdAndUp")
        v-row(style='float:left')
          MenuLine(v-if="$vuetify.breakpoint.mdAndUp")
      v-col( md="6" v-if="$vuetify.breakpoint.mdAndUp")
        v-row
          List(v-if="$vuetify.breakpoint.mdAndUp")
      v-col(cols="12"  v-if="$vuetify.breakpoint.smAndDown")
        v-row
          MobileList(v-if="$vuetify.breakpoint.smAndDown")
      v-spacer
      v-col.btn(cols="11" md="4" )
        v-row
          Contact
  v-col.footer
    v-row.footerlogo(align="end")
      v-spacer
      v-col(md="3")
        v-row
          FooterLogoMark
    v-row(justify="start" align="end")
      v-col(md="2")
        v-row.twitter
          BottomBtn
</template>
<script>
import FooterLogoMark from '@/components/Home/FooterLogoMark.vue'
import List from '@/components/Home/List.vue'
import MenuLine from '@/components/Home/MenuLine.vue'
import Contact from '@/components/Home/Contact.vue'
import BottomBtn from '@/components/Home/BottomBtn.vue'
import MobileList from '@/components/Home/MobileList.vue'
export default {
  name: 'Pj002',
  components: {
    FooterLogoMark,
    List,
    MenuLine,
    Contact,
    BottomBtn,
    MobileList
  },
  data: () => ({
    isActive: false,
    absolute: true,
    color: '#4593CC',
    opacity: 1.0
  }),
  methods: {
    toggleSwitch() {
      this.overlay = !this.overlay
    }
  }
}
</script>
<style>
.v-overlay__content {
  width: 100vw;
  height: 100vh;
  padding: -12px;
}
.main {
  float: left;
  width: 100vw;
  height: 80%;
}
.center {
  height: 80%;
}
.footer {
  height: 100%;
}
.footerlogo {
  height: 12%;
}
element.style {
  height: 30%;
}
.btn {
  margin-left: auto;
  margin-right: auto;
}
</style>
