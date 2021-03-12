<template>
  <div class="final-plate">
    <div class="left">
      <b></b><b></b><b></b><b></b>
      <span>黑科技提升</span>
      <div class="contain">
        <box-border :boxStyle="boxStyle6">
          <div class="contentdata">
            <div class="image">
              <img src="../../../../assets/img/icon1.png" alt="">
            </div>
            <div class="number">7000</div>
            <div class="name">机器人</div>
          </div>
        </box-border>
        <box-border :boxStyle="boxStyle6">
          <div class="contentdata">
            <div class="image image2">
              <img src="../../../../assets/img/icon2.png" alt="">
            </div>
            <div class="number">600</div>
            <div class="name">视频</div>
          </div>
        </box-border>
      </div>
    </div>
    <div class="right">
      <b></b><b></b><b></b><b></b>
      <span>报表输出</span>
      <div class="contain">
        <box-border :boxStyle="boxStyle6">
          <div class="contentdata">
            <div class="image image3">
              <img src="../../../../assets/img/icon3.png" alt="">
            </div>
            <div class="number">360</div>
            <div class="name">定制化报表</div>
          </div>
        </box-border>
        <box-border :boxStyle="boxStyle6">
          <div class="contentdata">
            <div class="image image3">
              <img src="../../../../assets/img/icon3.png" alt="">
            </div>
            <div class="number">600</div>
            <div class="name">共输出</div>
          </div>
        </box-border>
      </div>
    </div>
  </div>
</template>

<script>
import BoxBorder from '../../../common/BoxBorder.vue'
export default {
  components: { BoxBorder },
  name: 'FinalPlate',
  data() {
    return {
      boxStyle6:{
        width: .859375,
        height: .78125,
        borderColor: '#2691ff'
      }
    }
  },
}
</script>

<style scoped>
.final-plate {
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 24.2%;
}

.left,
.right {
  position: relative;
  width: 49.3%;
  height: 100%;
  background-color: #031428;
  padding: 2.5% 2%;
}

.left b,
.right b {
  display: inline-block;
  position: absolute;
  width: .104167rem;
  height: .104167rem;
  background: url('../../../../assets/img/tl.png') no-repeat;
  background-size: 100% 100%;
}

.left b:nth-child(1) {
  top: 0;
  left: 0;
}

.left b:nth-child(2) {
  top: 0;
  right: 0;
  background-image: url('../../../../assets/img/tr.png');

}
.left b:nth-child(3) {
  bottom: 0;
  left: 0;
  background-image: url('../../../../assets/img/bl.png');

}
.left b:nth-child(4) {
  bottom: 0;
  right: 0;
  background: url('../../../../assets/img/br.png');
}

.right b:nth-child(1) {
  top: 0;
  left: 0;
}

.right b:nth-child(2) {
  top: 0;
  right: 0;
  background-image: url('../../../../assets/img/tr.png');

}
.right b:nth-child(3) {
  bottom: 0;
  left: 0;
  background-image: url('../../../../assets/img/bl.png');

}
.right b:nth-child(4) {
  bottom: 0;
  right: 0;
  background-image: url('../../../../assets/img/br.png');
}

.contain {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 90%;
}

.contentdata {
  display: flex;
  height: 100%;
  padding:  8px;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}

.contentdata .image {
  width: .299479rem;
  height: .299479rem;
}

.contentdata .image2 {
  width: .279948rem;
  height: .227865rem;
}

.contentdata .image3 {
  width: .195313rem;
  height: .234375rem;
}

.image img {
  width: 100%;
  height: 100%;
}

.contentdata .number {
  font-size: .104167rem;
  color: #FFD200;
}

.contentdata .name {
  font-size: .091146rem;
}

.boxBgc {
  background-color: #031428;
}

</style>