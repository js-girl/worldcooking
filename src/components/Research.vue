<template>
  <div class="button">
    <br />
    <div class="top">レストランを探す</div>
    <div class="middle">
      <button v-on:click="wasyoku">和食</button>
      <button v-on:click="yousyoku">洋食</button>
      <button v-on:click="italian">イタリアン</button>
      <button v-on:click="china">中華</button>
      <button v-on:click="koria">韓国料理</button>
      <button v-on:click="asia">アジア・エスニック料理</button>
      <button v-on:click="kakkoku">各国料理</button>
    </div>
    <div class="end">
      <div v-if="genre === 'wasyoku'">
        <Wasyoku />
      </div>
      <div v-else-if="genre === 'yousyoku'">
        <Yousyoku />
      </div>
      <div v-else-if="genre === 'italian'">
        <Hotpepper />
      </div>
      <div v-else-if="genre === 'china'">
        <China />
      </div>
      <div v-else-if="genre === 'koria'">
        <Koria />
      </div>
      <div v-else-if="genre === 'asia'">
        <Asia />
      </div>
      <div v-else-if="genre === 'kakkoku'">
        <Kakkoku />
      </div>
      <div v-else></div>
    </div>
  </div>
</template>

<script>
import Wasyoku from "./Wasyoku.vue"
import Yousyoku from "./Yousyoku.vue"
import Hotpepper from "./Hotpepper.vue"
import China from "./China.vue"
import Koria from "./Koria.vue"
import Asia from "./Asia.vue"
import Kakkoku from "./Kakkoku.vue"

export default {
  components: {
    Wasyoku,
    Yousyoku,
    Hotpepper,
    China,
    Koria,
    Asia,
    Kakkoku,
  },
  data() {
    return {
      genre: "",
    }
  },
  methods: {
    wasyoku: function () {
      this.genre = "wasyoku"
    },
    yousyoku: function () {
      this.genre = "yousyoku"
    },
    italian: function () {
      this.genre = "italian"
    },
    china: function () {
      this.genre = "china"
    },
    koria: function () {
      this.genre = "koria"
    },
    asia: function () {
      this.genre = "asia"
    },
    kakkoku: function () {
      this.genre = "kakkoku"
    },
  },
}
</script>

<style>
.button {
  margin: 0 auto;
  min-height: 10vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.top {
  font-size: 30px;
  display: flex;
  align-items: center;
  text-align: center;
}

.middle {
  position: relative;
  display: inline-block;
  font-weight: bold;
  padding: 0.5em 1em;
  text-decoration: none;
  border-left: solid 4px #668ad8;
  border-right: solid 4px #668ad8;
  color: #668ad8;
  text-shadow: 0 0 5px white;
  padding: 0.5em 1em;
  background: repeating-linear-gradient(
    -45deg,
    #cce7ff,
    #cce7ff 3px,
    #e9f4ff 3px,
    #e9f4ff 7px
  );
  transition: 0.4s;
}
.middle:hover {
  background: repeating-linear-gradient(
    -45deg,
    #cce7ff,
    #cce7ff 5px,
    #e9f4ff 5px,
    #e9f4ff 9px
  );
}
.end {
  margin: 0 auto;
  min-height: 10vh;
  display: flex;
  justify-content: column;
  align-items: center;
  text-align: center;
}
</style>
