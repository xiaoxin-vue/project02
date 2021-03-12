<template>
  <div class="main-plate">
    <div class="main-bg">
      <img src="../../../../assets/img/bg.png" alt="">
    </div>
    <div class="boxpol"></div>
    <click-header :textArray="textArray1"/>
    <div class="gearBox">
      <gear :gearData="gear1" class="mtop"/>
      <gear :gearData="gear2"/>
      <gear :gearData="gear3" class="mtop"/>
    </div>
    <div class="around">
      <div class="circle">
      </div>
    </div>
  </div>
</template>

<script>
import ClickHeader from '../../../common/ClickHeader.vue'
import Gear from '../../../common/Gear.vue'
export default {
  name: 'MainPlate',
  data() {
    return {
      textArray1: [
        '领导看板',
        '数据分析',
        '基层分析',
        '数据中心'
      ],
      gear1: {
        text: '任务',
        clockWise: true
      },
      gear2: {
        text:'流程',
        clockWise: false
      },
      gear3: {
        text: '人',
        clockWise: true
      }
    }
  },
  components: {
   ClickHeader, 
   Gear
  },
}
</script>

<style scoped>
.main-plate {
  width: 100%;
  height: 40.2%;
  background-size: 100% 100%;
}

.main-bg {
  position: absolute;
  top: 0;
  left: 30%;
  width: 4.042969rem;
  height: 3.098958rem;
  z-index: 10;
}

.main-bg img {
  width: 100%;
  height: 100%;
}

.boxpol {
  position: absolute;
  top: .555469rem;
  left: 24.78%;
  /* 765px */
  width: 50.34%;
  /* 60px */
  height: .360625rem;
  background: url('../../../../assets/img/nav_bg1.png') no-repeat;
  background-size: 100% 100%;
}

.gearBox {
  position: relative;
  display: flex;
  justify-content: center;
  z-index: 12;
  margin-top: .130208rem;
}

.mtop {
  position: relative;
  margin-top: .250417rem;
  left: -0.052083rem;
}

.mtop:nth-child(1) {
  left: 0.052083rem;
}

.around {
  position: absolute;
  /* top: 0;
  left: 0; */
  /* top: 39%; */
  top: 1.102087rem;
  left: 37.8%;
  transform: rotateX(80deg);
  z-index: 20;
}

.circle {
  width: 2.604167rem;
  height: 2.604167rem;
  background: url('../../../../assets/img/ttround.png') no-repeat center center;
  background-size: contain;
  animation: round 5s linear infinite;
}

@keyframes round{
  0%{
    transform: rotateZ(0deg);/*从0度开始*/
  }
  100%{
    transform: rotateZ(360deg);/*360度结束*/
  }
}
</style>