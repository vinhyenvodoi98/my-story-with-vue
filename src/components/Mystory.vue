<template>
  <div class="mystory">
    <div class="stage">
      <div class="wrapper">
        <div class="slash"></div>
        <div class="sides">
          <div class="side"></div>
          <div class="side"></div>
          <div class="side"></div>
          <div class="side"></div>
        </div>
        <div class="text">
          <div class="text--backing">Mystory</div>
          <div class="text--left">
            <div class="inner">Mystory</div>
          </div>
          <div class="text--right">
            <div class="inner">Mystory</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
*,
*:before,
*:after {
  box-sizing: border-box;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
html,
body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
  background: #222;
  font-family: Josefin Sans, Helvetica, Helvetica Neue, Arial, sans-serif;
  font-size: 16px;
  font-weight: normal;
}
.stage {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.wrapper {
  position: relative;
  color: #fff;
  font-size: 2.5rem;
  text-transform: uppercase;
  letter-spacing: 0.25rem;
  padding-top: 0.65rem;
  padding-left: 0.5rem;
  padding-right: 0.36rem;
  padding-bottom: 0.2rem;
}
.slash {
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
  transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
  -webkit-transform-origin: center center;
  transform-origin: center center;
  width: 0.15rem;
  height: 145%;
  background: #fff;
  z-index: 4;
  -webkit-animation: slash 6s ease-in infinite;
  animation: slash 6s ease-in infinite;
}
/* mau phu thuoc vao backgroup */
.slash:before {
  content: "";
  display: block;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  width: 0.75rem;
  height: 120%;
  background: #3cbc9c;
  z-index: -1;
}
.slash:after {
  content: "";
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #fff;
}
.sides {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  overflow: hidden;
}
.sides .side {
  position: absolute;
  background: #fff;
}
.sides .side:nth-child(1) {
  top: 0;
  left: 0;
  width: 100%;
  height: 0.15rem;
  -webkit-transform: translateX(-101%);
  transform: translateX(-101%);
  -webkit-animation: side-top ease 6s infinite;
  animation: side-top ease 6s infinite;
}
.sides .side:nth-child(2) {
  top: 0;
  right: 0;
  width: 0.15rem;
  height: 100%;
  -webkit-transform: translateY(-101%);
  transform: translateY(-101%);
  -webkit-animation: side-right ease 6s infinite;
  animation: side-right ease 6s infinite;
}
.sides .side:nth-child(3) {
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.15rem;
  -webkit-transform: translateX(101%);
  transform: translateX(101%);
  -webkit-animation: side-bottom ease 6s infinite;
  animation: side-bottom ease 6s infinite;
}
.sides .side:nth-child(4) {
  top: 0;
  left: 0;
  width: 0.15rem;
  height: 100%;
  -webkit-transform: translateY(101%);
  transform: translateY(101%);
  -webkit-animation: side-left ease 6s infinite;
  animation: side-left ease 6s infinite;
}
.text {
  position: relative;
}
.text--backing {
  opacity: 0;
}
.text--left {
  position: absolute;
  top: 0;
  left: 0;
  width: 51%;
  height: 100%;
  overflow: hidden;
}
.text--left .inner {
  -webkit-transform: translateX(100%);
  transform: translateX(100%);
  -webkit-animation: text-left 6s ease-in-out infinite;
  animation: text-left 6s ease-in-out infinite;
}
.text--right {
  position: absolute;
  top: 0;
  right: 0;
  width: 50%;
  height: 100%;
  overflow: hidden;
}
.text--right .inner {
  -webkit-transform: translateX(-200%);
  transform: translateX(-200%);
  -webkit-animation: text-right 6s ease-in-out infinite;
  animation: text-right 6s ease-in-out infinite;
}
@-webkit-keyframes slash {
  0% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
  }
  6% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(1);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(1);
  }
  13% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(1);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(1);
  }
  16.6% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
  }
  100% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
  }
}
@keyframes slash {
  0% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
  }
  6% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(1);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(1);
  }
  13% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(1);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(1);
  }
  16.6% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
  }
  100% {
    -webkit-transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
    transform: translate(-50%, -50%) rotate(-24deg) scaleY(0);
  }
}
@-webkit-keyframes text-left {
  0% {
    -webkit-transform: translateX(100%);
    transform: translateX(100%);
  }
  10% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  58% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  70% {
    -webkit-transform: translateX(-200%);
    transform: translateX(-200%);
  }
  100% {
    -webkit-transform: translateX(-200%);
    transform: translateX(-200%);
  }
}
@keyframes text-left {
  0% {
    -webkit-transform: translateX(100%);
    transform: translateX(100%);
  }
  10% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  58% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  70% {
    -webkit-transform: translateX(-200%);
    transform: translateX(-200%);
  }
  100% {
    -webkit-transform: translateX(-200%);
    transform: translateX(-200%);
  }
}
@-webkit-keyframes text-right {
  0% {
    -webkit-transform: translateX(-200%);
    transform: translateX(-200%);
  }
  10% {
    -webkit-transform: translateX(-100%);
    transform: translateX(-100%);
  }
  58% {
    -webkit-transform: translateX(-100%);
    transform: translateX(-100%);
  }
  70% {
    -webkit-transform: translateX(-300%);
    transform: translateX(-300%);
  }
  100% {
    -webkit-transform: translateX(-300%);
    transform: translateX(-300%);
  }
}
@keyframes text-right {
  0% {
    -webkit-transform: translateX(-200%);
    transform: translateX(-200%);
  }
  10% {
    -webkit-transform: translateX(-100%);
    transform: translateX(-100%);
  }
  58% {
    -webkit-transform: translateX(-100%);
    transform: translateX(-100%);
  }
  70% {
    -webkit-transform: translateX(-300%);
    transform: translateX(-300%);
  }
  100% {
    -webkit-transform: translateX(-300%);
    transform: translateX(-300%);
  }
}
@-webkit-keyframes side-top {
  0%,
  14% {
    -webkit-transform: translateX(-101%);
    transform: translateX(-101%);
  }
  24%,
  55% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  65% {
    -webkit-transform: translateX(101%);
    transform: translateX(101%);
  }
  100% {
    -webkit-transform: translateX(101%);
    transform: translateX(101%);
  }
}
@keyframes side-top {
  0%,
  14% {
    -webkit-transform: translateX(-101%);
    transform: translateX(-101%);
  }
  24%,
  55% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  65% {
    -webkit-transform: translateX(101%);
    transform: translateX(101%);
  }
  100% {
    -webkit-transform: translateX(101%);
    transform: translateX(101%);
  }
}
@-webkit-keyframes side-right {
  0%,
  14%,
  23% {
    -webkit-transform: translateY(-101%);
    transform: translateY(-101%);
  }
  30%,
  62% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  72% {
    -webkit-transform: translateY(101%);
    transform: translateY(101%);
  }
  100% {
    -webkit-transform: translateY(101%);
    transform: translateY(101%);
  }
}
@keyframes side-right {
  0%,
  14%,
  23% {
    -webkit-transform: translateY(-101%);
    transform: translateY(-101%);
  }
  30%,
  62% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  72% {
    -webkit-transform: translateY(101%);
    transform: translateY(101%);
  }
  100% {
    -webkit-transform: translateY(101%);
    transform: translateY(101%);
  }
}
@-webkit-keyframes side-bottom {
  0%,
  14%,
  24%,
  28% {
    -webkit-transform: translateX(101%);
    transform: translateX(101%);
  }
  37%,
  70% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  79% {
    -webkit-transform: translateX(-101%);
    transform: translateX(-101%);
  }
  100% {
    -webkit-transform: translateX(-101%);
    transform: translateX(-101%);
  }
}
@keyframes side-bottom {
  0%,
  14%,
  24%,
  28% {
    -webkit-transform: translateX(101%);
    transform: translateX(101%);
  }
  37%,
  70% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
  }
  79% {
    -webkit-transform: translateX(-101%);
    transform: translateX(-101%);
  }
  100% {
    -webkit-transform: translateX(-101%);
    transform: translateX(-101%);
  }
}
@-webkit-keyframes side-left {
  0%,
  14%,
  24%,
  34%,
  35% {
    -webkit-transform: translateY(101%);
    transform: translateY(101%);
  }
  44%,
  79% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  86% {
    -webkit-transform: translateY(-101%);
    transform: translateY(-101%);
  }
  100% {
    -webkit-transform: translateY(-101%);
    transform: translateY(-101%);
  }
}
@keyframes side-left {
  0%,
  14%,
  24%,
  34%,
  35% {
    -webkit-transform: translateY(101%);
    transform: translateY(101%);
  }
  44%,
  79% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  86% {
    -webkit-transform: translateY(-101%);
    transform: translateY(-101%);
  }
  100% {
    -webkit-transform: translateY(-101%);
    transform: translateY(-101%);
  }
}
</style>

<script>
export default {
  name: "mystory",
  props: {
    msg: String
  }
};
</script>
