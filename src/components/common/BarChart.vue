<template>
  <div class="bar">
    <div class="linebox"><span class="line-text">100</span></div>
    <div class="linebox"><span class="line-text">80</span></div>
    <div class="linebox"><span class="line-text">60</span></div>
    <div class="linebox"><span class="line-text">40</span></div>
    <div class="linebox"><span class="line-text">20</span></div>
    <span class="text-zero">0</span>
    <div class="bar-chart">
      <span class="item rect1"><em class="item-text">白塔岭</em></span>
      <span class="item rect2"><em class="item-text">水澄桥</em></span>
      <span class="item rect3"><em class="item-text">海月桥</em></span>
      <span class="item rect4"><em class="item-text">美政桥</em></span>
      <span class="item rect5"><em class="item-text">紫花埠</em></span>
      <span class="item rect6"><em class="item-text">复兴街</em></span>
      <span class="item rect7"><em class="item-text">馒头山</em></span>
      <span class="item rect8"><em class="item-text">玉皇山</em></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BarChart'
}
</script>

<style scoped>
.bar {
  position: relative;
  width: 62%;
  height: 100%;
  border-left: 1px solid #0f94f9;
  border-bottom: 1px solid #0f94f9;
}

.linebox {
  position: relative;
  width: 100%;
  height: 20%; 
  border-top: 1px solid #091e3b;
}

.linebox .line-text {
  display: inline-block;
  width: .143229rem;
  height: .071615rem;
  position: absolute;
  left: -0.195313rem;
  top: -0.058594rem;
  font-size: .078125rem;
  color: #878b90;
  text-align: right;
}

.text-zero {
  display: inline-block;
  width: .143229rem;
  height: .071615rem;
  position: absolute;
  bottom: -0.026042rem;
  left: -0.195313rem;
  font-size: .078125rem;
  color: #878b90;
  text-align: right;
}

.bar-chart {
  position: absolute;
  top: 0;
  left: -0.00651rem;
  display: flex;
  width: 100%;
  height: 100%;
  /* space-evenly 均匀排列每个元素,每个元素之间的间隔相等 */
  justify-content: space-around;
  align-items: flex-end;
}

.item {
  position: relative;
  width: 7%;
  background-color: #009eff;
}
.rect1 {
  height: 44%;
}
.rect2 {
  height: 38%;
}
.rect3 {
  height: 39%;
}
.rect4 {
  height: 46%;
}
.rect5{
  height: 49%;
}
.rect6 {
  height: 68%;
}
.rect7 {
  height: 62%;
}
.rect8{
  height: 24%;
}

.item-text {
  display: inline-block;
  position: absolute;
  left: -0.026042rem;
  bottom: -0.104167rem;
  font-style: normal;
  width: .195313rem;
  height: .078125rem;
  font-size: .052083rem;
  color: #878b90;
}

/* @media screen and (min-width: 1024px) {
  .item-text  {
    transform: scale(0.5);
  }
} */
</style>