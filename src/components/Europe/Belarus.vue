<template>
  <!-- 変更する箇所に！ついています。基本的にはこれをコピーして使い回してください。 -->
  <div id="zentai" v-show="showContent">
    <button class="batsu" v-on:click="close">×</button>
    <div id="gohan">
      <div class="content">
        <div class="title">ドラニキ</div>
        <div class="kuni">ベラルーシ</div>
      </div>
    </div>
    <div id="gazou">
      <div class="content">
        <!-- 画像を変更。imagesフォルダに追加してください。 -->
        <img src="../../images/noimage.jpg" width="280px" />
      </div>
    </div>

    <div id="story">
      <!-- 説明を変更 -->
      <div class="content">
        <div class="title">ストーリー</div>
        <div class="setumei">
          ジャガイモのパンケーキのような料理。
          生のジャガイモをすりおろして、みじん切りのたまねぎ、卵、少量の小麦粉と混ぜ合わせ、多めの油を敷いたフライパンでこんがりきつね色に焼きます。
          熱いうちに「スメタナ」と呼ばれるサワークリームを添えていただきます。
        </div>
      </div>
    </div>

    <div id="omise">
      <div class="content">
        <!-- APIリンク#部分を変えてね -->
        <div class="mb-10">
          <a
            href="https://www.google.co.jp/maps/place/%E3%83%99%E3%83%A9%E3%83%AB%E3%83%BC%E3%82%B7%E5%AE%B6%E5%BA%AD%E6%96%99%E7%90%86+%E3%83%9F%E3%83%B3%E3%82%B9%E3%82%AF%E3%81%AE%E5%8F%B0%E6%89%80/@35.6500146,139.663927,11.14z/data=!4m5!3m4!1s0x60188b9bbfb063d3:0x34351a421e0414c0!8m2!3d35.6596859!4d139.7422363?authuser=0"
            class="btn btn-mod btn-border btn-circle btn-large"
            >お店を探す</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showContent: true,
    }
  },
  methods: {
    close: function () {
      this.showContent = false
    },
  },
}
</script>

<style scoped>
#zentai {
  background-color: #fffff9;
  width: 300px;
  border-radius: 20px;
  padding: 10px;
  font-family: TsukuARdGothic-Regular;
  box-shadow: 4px 4px #f5f5f5;
}
a {
  text-decoration: none;
  color: black;
}
img {
  vertical-align: bottom;
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 5px;
  margin: 5x;
}
.title {
  font-size: 23px;
  font-weight: bold;
  text-align: center;
  width: 200px;
  border-bottom: solid 2px;
}
#gohan {
  width: 300px;
  background-color: #ffc9d2;
  color: #fffff5;
  border-radius: 3px;
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
/* ばつボタン */
.batsu {
  font-size: 100%; /*ボタンの大きさ*/
  font-weight: bold;
  border: 1px solid #999;
  color: #999;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 100%;
  width: 1.5em;
  line-height: 1.3em;
  cursor: pointer;
  transition: 0.2s;
}

.batsu:hover {
  background: #333;
  border-color: #333;
  color: #fff;
}
</style>
