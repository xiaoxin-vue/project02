<template>
  <div class="personnel">
    <b></b><b></b><b></b><b></b>
    <span class="personnel-text">人口赋能</span>
    <div class="content">
      <div class="left">
        <box-border :boxStyle="boxStyle4">
          <div class="boxContent">
            <p class="learn-time">6000</p>
            <p class="learn-text">
              学习时长(小时)
            </p>
          </div>
        </box-border>
        <box-border :boxStyle="boxStyle4">
          <div class="boxContent">
            <p class="learn-time">75</p>
            <p class="learn-text">
              考试成绩(平均分)
            </p>
          </div>
        </box-border>
      </div>
      <div class="right">
        <span class="text">技能排行</span>
        <progress-demo :proInfo="proInfo90"/>
        <progress-demo :proInfo="proInfo80"/>
        <progress-demo :proInfo="proInfo70"/>
        <progress-demo :proInfo="proInfo60"/>
        <progress-demo :proInfo="proInfo50"/>
        <progress-demo :proInfo="proInfo40"/>
      </div>
    </div>
  </div>
</template>

<script>
import BoxBorder from '../../../common/BoxBorder.vue'
import ProgressDemo from '../../../common/ProgressDemo.vue'

export default {
  components: { BoxBorder, ProgressDemo },
  name: 'Personnel',
  data() {
    return {
      boxStyle4:{
        width: .664063,
        height: .664063,
        borderColor: '#409eff'
      },
      proInfo90: {
        num: 90,
        proText: '白塔岭'
      },
      proInfo80: {
        num: 80,
        proText: '水橙桥'
      },
      proInfo70: {
        num: 70,
        proText: '海月桥'
      },
      proInfo60: {
        num: 60,
        proText: '美政桥'
      },
      proInfo50: {
        num: 50,
        proText: '紫花埠'
      },
      proInfo40: {
        num: 40,
        proText: '复兴街'
      }
    }
  },
}
</script>

<style scoped>
.personnel {
  position: relative;
  width: 100%;
  height: 34%;
  padding: 4%;
  background-color: #031428;
}

.personnel b {
  display: inline-block;
  position: absolute;
  width: .104167rem;
  height: .104167rem;
  background: url('../../../../assets/img/tl.png') no-repeat;
  background-size: 100% 100%;
}

.personnel b:nth-child(1) {
  top: 0;
  left: 0;
}

.personnel b:nth-child(2) {
  top: 0;
  right: 0;
  background-image: url('../../../../assets/img/tr.png');
}
.personnel b:nth-child(3) {
  bottom: 0;
  left: 0;
  background-image: url('../../../../assets/img/bl.png');

}
.personnel b:nth-child(4) {
  bottom: 0;
  right: 0;
  background-image: url('../../../../assets/img/br.png');
}

.content {
  display: flex;
  justify-content: space-between;
  height: 85%;
  margin-top: .105104rem;
}

.content .left {
  display: flex;
  height: 100%;
  flex-direction: column;
  justify-content: space-between;
}

.content .right {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.text {
  line-height: 0;
  opacity: 0.5;
}

.boxContent {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
}

.left .learn-time {
  width: .507813rem;
  height: .195313rem;
  font-size: .123698rem;
  color: #FFD200;
  text-align: center;
}

.left .learn-text {
  width: .442708rem;
  font-size: .084635rem;
  text-align: center;
}
</style>