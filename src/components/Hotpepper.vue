<template>
  <div>
    <html lang="ja">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <meta http-equiv="X-UA-Compatible" content="ie=edge" />
        <title>Fetch JSON</title>
      </head>
      <body>
        <h1>{{ date }}</h1>
        <div>
          <img src="" alt="お店の名前" id="food-image" />
        </div>
      </body>
    </html>
  </div>
</template>

<script>
const imageElement = document.getElementById("food-image");

fetch(
  "http://webservice.recruit.co.jp/hotpepper/gourmet/v1/?key=703a952c5ae9eaa7&large_area=Z011"
)
  .then((res) => {
    return res.json();
  })
  .then((data) => {
    imageElement.src = data.message;
  });
</script>

<style></style>
