<template>
  <div id="genre">
    🍽 shop list 🍽
    <div id="shop">
      <div v-for="food in all" :key="food.id">
        <img :src="food.logo_image" alt="" />

        <br />
        <a v-bind:href="food.urls.pc">{{ food.name }}</a>
      </div>
    </div>
    <br />
    Powered by
    <a href="http://webservice.recruit.co.jp/">ホットペッパー Webサービス</a>
  </div>
</template>

<script>
export default {
  data() {
    return { all: [] }
  },
  methods: {
    getrestaurant: function () {
      fetch(
        "https://webservice.recruit.co.jp/hotpepper/gourmet/v1/?key=703a952c5ae9eaa7&large_area=Z011&genre=G006&format=json"
      )
        .then((res) => {
          return res.json()
        })
        .then((value) => {
          this.all = value.results.shop
        })

      // this.axios
      //   .get(
      //     "hotpepper/gourmet/v1/?key=703a952c5ae9eaa7&large_area=Z011&genre=G006&format=json"
      //   )
      //   .then((res) => res.data)
      //   .then((value) => {
      //     this.all = value.results.shop

      //     console.log(value)
      //     console.log(value.results)
      //     console.log(value.results.shop)
      //   })
    },
  },
  mounted() {
    this.getrestaurant()
  },
}
</script>

<style>
#genre {
  font-size: 20px;
  font-family: Avenir;
  margin-bottom: 20px;
}

#shop {
  background: #d2e7fc;
  font-family: Avenir;
  text-align: center;
  color: #046b62;
  padding-top: 50px;
  padding-bottom: 50px;
}
</style>
