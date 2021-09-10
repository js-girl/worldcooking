<template>
  <div id="app">
    <div class="ue">
      <h1>World cooking</h1>
    </div>
    <div section="content1">
      <GoogleMap />
    </div>
    <div section="content2">
      <div class="main-coppy">
        <h2>世界の料理を <br />日本で楽しもう。</h2>
      </div>
      <div class="sub-coppy">世界の料理、集めました。</div>
      <div class="main-pic">
        <img class="pict" src="./images/wasyoku.jpg" width="500px" />
      </div>
      <div class="about">
        このwebサイトでは、様々な国の伝統料理を紹介しています。
        <br />お店を探すをクリックすると、日本で楽しめるレストランが表示されます。
        <br />コロナ禍でも海外旅行気分を味わえます。
      </div>
    </div>
    <div section="content3">
      <Slide />
    </div>

    <footer><small>&copy;js-girls.2021</small></footer>
  </div>
</template>

<script>
import GoogleMap from "./components/Map.vue"
import Slide from "./components/Slide.vue"

export default {
  name: "App",
  components: {
    GoogleMap,
    Slide,
  },
}
</script>

<style>
footer {
  display: flex;
  justify-content: center;
  margin-top: 5px;
}
#app {
  font-family: TsukuARdGothic-Regular;
  display: flex;
  flex-direction: column;
}
.ue {
  height: 100px;
  padding-left: 10%;
  font-size: 28px;
  margin-bottom: 20px;
}
.content1 {
  display: flex;
}
.content2 {
  display: flex;
  align-items: center;
  justify-content: center;
}
.main-coppy {
  margin-left: 20%;
  font-size: 30px;
}
.sub-coppy {
  margin-left: 30%;
}
.main-pic {
  margin-top: 50px;
  margin-left: 50%;
}
.pict {
  box-shadow: -40px 40px #ffc9d2;
}

.about {
  margin-top: 70px;
  width: 70%;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}

.sec-title {
  margin-top: 50px;
  text-align: center;
}
.content3 {
  margin-top: 10px;
  margin-bottom: 10px;
}

/* ボタン */
.mb-10 {
  margin-top: 10px;
  margin-bottom: 30px;
}

.btn-mod,
a.btn-mod {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  padding: 4px 13px;
  color: #fff;
  background: rgba(34, 34, 34, 0.9);
  border: 2px solid transparent;
  font-size: 13px;
  font-weight: 400;
  text-transform: uppercase;
  text-decoration: none;
  letter-spacing: 2px;

  -webkit-border-radius: 0;
  -moz-border-radius: 0;
  border-radius: 0;

  -webkit-transition: all 0.2s cubic-bezier(0, 0, 0.58, 1);
  -moz-transition: all 0.2s cubic-bezier(0, 0, 0.58, 1);
  -o-transition: all 0.2s cubic-bezier(0, 0, 0.58, 1);
  -ms-transition: all 0.2s cubic-bezier(0, 0, 0.58, 1);
  transition: all 0.2s cubic-bezier(0, 0, 0.58, 1);
}
.btn-mod:hover,
.btn-mod:focus,
a.btn-mod:hover,
a.btn-mod:focus {
  font-weight: 400;
  color: rgba(255, 255, 255, 0.85);
  background: rgba(0, 0, 0, 0.7);
  text-decoration: none;
  outline: none;
}
.btn-mod:active {
  cursor: pointer !important;
}

.btn-mod.btn-large {
  padding: 12px 45px;
  font-size: 13px;
}
/* ==============================
   border黒枠ボタン
   ============================== */
.btn-mod.btn-border {
  color: #151515;
  border: 2px solid #ffc9d2;
  background: transparent;
}
.btn-mod.btn-border:hover,
.btn-mod.btn-border:focus {
  color: #fffffb;
  border-color: transparent;
  background: #ffc9d2;
}
</style>
