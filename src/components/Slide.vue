<template>
  <div class="slide">
    <ul class="slide-nav">
      <li class="slider"><img src="../images/afternoontea.jpg" /></li>
      <li class="slider"><img src="../images/antiq.jpg" /></li>
      <li class="slider"><img src="../images/asado.jpg" /></li>
      <li class="slider"><img src="../images/borushichi.jpg" /></li>
      <li class="slider"><img src="../images/chezz.jpg" /></li>
      <li class="slider"><img src="../images/curry.jpg" /></li>
      <li class="slider"><img src="../images/enpa.jpg" /></li>
      <li class="slider"><img src="../images/Escalgo.jpg" /></li>
      <li class="slider"><img src="../images/fejo.jpg" /></li>
      <li class="slider"><img src="../images/foo.jpg" /></li>
      <li class="slider"><img src="../images/humburger.jpg" /></li>
      <li class="slider"><img src="../images/Humms.jpg" /></li>
      <li class="slider"><img src="../images/borushichi.jpg" /></li>
      <li class="slider"><img src="../images/kebabu.jpg" /></li>
      <li class="slider"><img src="../images/kimuchi.jpg" /></li>
      <li class="slider"><img src="../images/Kuskus.jpg" /></li>
      <li class="slider"><img src="../images/mabo.jpg" /></li>
      <li class="slider"><img src="../images/meatpie.jpg" /></li>
      <li class="slider"><img src="../images/musaka.jpg" /></li>
      <li class="slider"><img src="../images/nashigoren.jpg" /></li>
      <li class="slider"><img src="../images/papurika.jpg" /></li>
      <li class="slider"><img src="../images/pirosiki.jpg" /></li>
      <li class="slider"><img src="../images/porenta.jpg" /></li>
      <li class="slider"><img src="../images/puting.jpg" /></li>
      <li class="slider"><img src="../images/Rurohan.jpg" /></li>
      <li class="slider"><img src="../images/sinigan.jpg" /></li>
      <li class="slider"><img src="../images/tacos.jpg" /></li>
      <li class="slider"><img src="../images/tomuyamu.jpg" /></li>
      <li class="slider"><img src="../images/wasyoku.jpg" /></li>
      <li class="slider"><img src="../images/winner.jpg" /></li>
    </ul>
    <ul class="slide-nav">
      <li class="slider"><img src="../images/afternoontea.jpg" /></li>
      <li class="slider"><img src="../images/antiq.jpg" /></li>
      <li class="slider"><img src="../images/asado.jpg" /></li>
      <li class="slider"><img src="../images/borushichi.jpg" /></li>
      <li class="slider"><img src="../images/chezz.jpg" /></li>
      <li class="slider"><img src="../images/curry.jpg" /></li>
      <li class="slider"><img src="../images/enpa.jpg" /></li>
      <li class="slider"><img src="../images/Escalgo.jpg" /></li>
      <li class="slider"><img src="../images/fejo.jpg" /></li>
      <li class="slider"><img src="../images/foo.jpg" /></li>
      <li class="slider"><img src="../images/humburger.jpg" /></li>
      <li class="slider"><img src="../images/Humms.jpg" /></li>
      <li class="slider"><img src="../images/borushichi.jpg" /></li>
      <li class="slider"><img src="../images/kebabu.jpg" /></li>
      <li class="slider"><img src="../images/kimuchi.jpg" /></li>
      <li class="slider"><img src="../images/Kuskus.jpg" /></li>
      <li class="slider"><img src="../images/mabo.jpg" /></li>
      <li class="slider"><img src="../images/meatpie.jpg" /></li>
      <li class="slider"><img src="../images/musaka.jpg" /></li>
      <li class="slider"><img src="../images/nashigoren.jpg" /></li>
      <li class="slider"><img src="../images/papurika.jpg" /></li>
      <li class="slider"><img src="../images/pirosiki.jpg" /></li>
      <li class="slider"><img src="../images/porenta.jpg" /></li>
      <li class="slider"><img src="../images/puting.jpg" /></li>
      <li class="slider"><img src="../images/Rurohan.jpg" /></li>
      <li class="slider"><img src="../images/sinigan.jpg" /></li>
      <li class="slider"><img src="../images/tacos.jpg" /></li>
      <li class="slider"><img src="../images/tomuyamu.jpg" /></li>
      <li class="slider"><img src="../images/wasyoku.jpg" /></li>
      <li class="slider"><img src="../images/winner.jpg" /></li>
    </ul>
  </div>
</template>

<script></script>

<style>
ul {
  list-style: none;
  display: flex;
}
img {
  width: 250px;
  height: 180px;
}
.slide {
  display: flex;
  max-width: 100vw;
  overflow: hidden;
}
@keyframes loop {
  0% {
    transform: translateX(100%);
  }
  to {
    transform: translateX(-100%);
  }
}
@keyframes loop2 {
  0% {
    transform: translateX(0%);
  }
  to {
    transform: translateX(-200%);
  }
}
.slide img:first-child {
  animation: loop 120s -60s linear infinite;
}

.slide img:last-child {
  animation: loop2 120s linear infinite;
}
.slide:hover ul {
  animation-play-state: paused;
}
</style>
