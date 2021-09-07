<template>
  <div id="app">
    <div section="content1">
      <GoogleMap />
      <Wasyoku />
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
    <div section="content31">
      <div class="sec-title">
        <h2>おすすめの世界料理</h2>
      </div>
      <div class="cbox-wrapper">
        <div class="cooking-box">
          <div class="pic">画像</div>
          <div class="mb-10">
            <a href="#" class="btn btn-mod btn-border btn-circle btn-large"
              >詳しく見る</a
            >
          </div>
        </div>
        <div class="cooking-box">
          <div class="pic">画像</div>
          <div class="mb-10">
            <a href="#" class="btn btn-mod btn-border btn-circle btn-large"
              >詳しく見る</a
            >
          </div>
        </div>
        <div class="cooking-box">
          <div class="pic">画像</div>
          <div class="mb-10">
            <a href="#" class="btn btn-mod btn-border btn-circle btn-large"
              >詳しく見る</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Wasyoku from "./components/EastAsia/Wasyoku.vue"
// import GoogleMap from "./components/Map.vue"
export default {
  name: "App",
  components: {
    Wasyoku,
    // GoogleMap,
  },
}
</script>

<style>
#app {
  font-family: TsukuARdGothic-Regular;
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
.cbox-wrapper {
  display: flex;
  justify-content: center;
  align-content: center;
}
.cooking-box {
  width: 300px;
  margin: 5px;
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
