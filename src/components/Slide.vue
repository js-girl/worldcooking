<template>
  <div class="slide">
    <ul class="slide-nav">
      <li class="slider">
        <img class="imgs" src="../images/afternoontea.jpg" />
      </li>
      <li class="slider"><img class="imgs" src="../images/antiq.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/asado.jpg" /></li>
      <li class="slider">
        <img class="imgs" src="../images/borushichi.jpg" />
      </li>
      <li class="slider"><img class="imgs" src="../images/chezz.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/curry.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/enpa.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/Escalgo.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/fejo.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/foo.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/humburger.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/Humms.jpg" /></li>
      <li class="slider">
        <img class="imgs" src="../images/borushichi.jpg" />
      </li>
      <li class="slider"><img class="imgs" src="../images/kebabu.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/kimuchi.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/Kuskus.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/mabo.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/meatpie.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/musaka.jpg" /></li>
      <li class="slider">
        <img class="imgs" src="../images/nashigoren.jpg" />
      </li>
      <li class="slider"><img class="imgs" src="../images/papurika.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/pirosiki.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/porenta.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/puting.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/Rurohan.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/sinigan.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/tacos.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/tomuyamu.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/wasyoku.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/winner.jpg" /></li>
    </ul>
    <ul class="slide-nav">
      <li class="slider">
        <img class="imgs" src="../images/afternoontea.jpg" />
      </li>
      <li class="slider"><img class="imgs" src="../images/antiq.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/asado.jpg" /></li>
      <li class="slider">
        <img class="imgs" src="../images/borushichi.jpg" />
      </li>
      <li class="slider"><img class="imgs" src="../images/chezz.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/curry.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/enpa.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/Escalgo.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/fejo.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/foo.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/humburger.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/Humms.jpg" /></li>
      <li class="slider">
        <img class="imgs" src="../images/borushichi.jpg" />
      </li>
      <li class="slider"><img class="imgs" src="../images/kebabu.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/kimuchi.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/Kuskus.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/mabo.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/meatpie.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/musaka.jpg" /></li>
      <li class="slider">
        <img class="imgs" src="../images/nashigoren.jpg" />
      </li>
      <li class="slider"><img class="imgs" src="../images/papurika.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/pirosiki.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/porenta.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/puting.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/Rurohan.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/sinigan.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/tacos.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/tomuyamu.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/wasyoku.jpg" /></li>
      <li class="slider"><img class="imgs" src="../images/winner.jpg" /></li>
    </ul>
  </div>
</template>

<script></script>

<style>
ul {
  list-style: none;
  display: flex;
}
.imgs {
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
  animation: loop 360s -180s linear infinite;
}

.slide img:last-child {
  animation: loop2 180s linear infinite;
}
.slide:hover ul {
  animation-play-state: paused;
}
</style>
