<template lang="pug">
div
  div.bottun
    v-item-group(
      v-for="btn in btns"
      v-bind:key="btn.message"
    )
      v-btn.release(
        retain-focus-on-click
        rounded
        outlined
        x-large
        :categories="categories"
        @click="click( btn.id )")  {{ btn.message }}
  div
    v-card.list(
      color='#FFFFFF'
      flat
      outlined
    )
      v-list-item-content(
        v-for="list in lists"
        v-bind:key="list.index"
        outlined
      )
        v-list-item-content
          v-list-item-line.line {{ list.date  }}|
            nobr.newslogo {{ list.category }}
        v-list-item-content
          v-list-item-line.title {{ list.title }}
        v-divider.listLines
  div.text-center
    v-pagination(
      v-model="page"
      :length="length"
      @input = "pageChange"
      color='#4593CC'
      light

    )
</template>
<script>
import axios from 'axios'
export default {
  data: () => ({
    name: 'news',
    btns: [
      {
        id: 0,
        message: 'プレスリリース'
      },
      {
        id: 1,
        message: 'ニュース'
      },
      {
        id: 2,
        message: 'リクルート'
      },
      {
        id: 3,
        message: '勉強会'
      }
    ],
    items: [],
    page: 1,
    pageSize: 10,
    length: 0,
    lists: [],
    displayLists: []
  }),
  methods: {
    click(categoryId) {
      this.displayLists = this.items.filter(
        (value) => value.categoryId === categoryId
      )
      this.length = Math.ceil(this.displayLists.length / this.pageSize)
      this.lists = this.displayLists.slice(0, this.pageSize)
    },
    pageChange(pageNumber) {
      this.lists = this.displayLists.slice(
        this.pageSize * (pageNumber - 1),
        this.pageSize * pageNumber
      )
      this.pageLength()
    },
    pageLength() {
      this.length = Math.ceil(this.displayLists.length / this.pageSize)
    }
  },
  mounted() {
    axios
      .get('https://jsonplaceholder.typicode.com/posts/')
      .then((response) => {
        this.items = response.data
        this.items.forEach((item) => {
          const itemCategoryId = Number(item.id) % 4
          let btnsBox = '勉強会'
          this.btns.forEach((btn) => {
            if (btn.id === itemCategoryId) {
              btnsBox = btn.message
            }
          })
          item.category = btnsBox
          item.date = '2020/08/20'
          item.categoryId = itemCategoryId
        })
        console.log(this.items)
        this.displayLists = this.items
        this.length = Math.ceil(this.displayLists.length / this.pageSize)
        this.lists = this.displayLists.slice(0, this.pageSize)
      })
  }
}
</script>
<style scoped lang="scss">
.bottun {
  background-color: #4492cb;
  width: 100%;
  height: 15%;
  top: -10%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.list {
  padding: 5%;
  width: 800px;
  height: 1000px;
}
.release {
  margin: 7px;
}
.line {
  color: #bcbbbb;
  font: normal 12px/10px 'Noto Sans Javanese';
}
.newslogo {
  color: black;
}
.listLines {
  color: '#BCBBBB';
}
.title {
  font: 2px/2px Hiragino Kaku Gothic Std;
  font-size: 3px;
  color: #171717;
}
</style>
