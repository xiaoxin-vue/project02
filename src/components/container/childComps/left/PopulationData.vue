<template>
  <div class="population-data">
    <b></b><b></b><b></b><b></b>
    <span class="population-text">人口数据</span>
    <div class="box-zero">
      <span class="population-total">总人口</span>
      <div class="num-total">
        <div class="num">
          5
        </div>
        <div class="num">
          5
        </div>
        <div class="num">
          5
        </div>
        <div class="num">
          ,
        </div>
        <div class="num">
          5
        </div>
        <div class="num">
          5
        </div>
        <div class="num">
          5
        </div>
      </div>
    </div>
    <div class="box-one">
      <box-border :boxStyle="boxStyle1">
        <div class="box-info">
          <p class="color-blue">5,000</p>
          <p>青少年</p>
        </div>
      </box-border>
      <box-border :boxStyle="boxStyle1">
        <div class="box-info">
          <p class="color-blue">5,000</p>
          <p>中年</p>
        </div>
      </box-border>
      <box-border :boxStyle="boxStyle1">
        <div class="box-info">
          <p class="color-blue">5,000</p>
          <p>妇女</p>
        </div>
      </box-border>
      <box-border :boxStyle="boxStyle1">
        <div class="box-info">
          <p class="color-blue">5,000</p>
          <p>老人</p>
        </div>
      </box-border>
    
    </div>
    <div class="box-two">
      <box-border :boxStyle="boxStyle2" class="box-two-border">
        <div class="box-info ">
          <p class="color-green">5,000</p>
          <p>网格人员</p>
        </div>
      </box-border>
      <box-border :boxStyle="boxStyle2" class="box-two-border">
        <div class="box-info">
          <p class="color-green">5,000</p>
          <p>社工</p>
        </div>
      </box-border>
    </div>
    <div class="box-three">
      <box-border :boxStyle="boxStyle3" class="box-three-border">
        <div class="box-info">
          <p class="color-yellow">5,000</p>
          <p>重点人群</p>
        </div>
      </box-border>
      <box-border :boxStyle="boxStyle3" class="box-three-border">
        <div class="box-info">
          <p class="color-yellow">5,000</p>
          <p>帮扶人群</p>
        </div>
      </box-border>
      <box-border :boxStyle="boxStyle3" class="box-three-border">
        <div class="box-info">
          <p class="color-yellow">5,000</p>
          <p>标签人群</p>
        </div>
      </box-border>
    </div>
  </div>
</template>

<script>
import BoxBorder from '../../../common/BoxBorder.vue'

export default {
  name: 'PopulationData',
  data() {
    return {
      boxStyle1: {
        width: .546875,
        height: .375,
        borderColor: '#2691ff'
      },
      boxStyle2: {
        width: .546875,
        height: .375,
        borderColor: '#03fab3'
      },
      boxStyle3: {
        width: .546875,
        height: .375,
        borderColor: '#ffd200'
      }
    }
  },
  components: {
    BoxBorder 
  }
}
</script>

<style scoped>
.population-data {
  position: relative;
  width: 100%;
  height: 34%;
  padding: 4%;
  background-color: #031428;
}

.population-data b {
  display: inline-block;
  position: absolute;
  width: .104167rem;
  height: .104167rem;
  background: url('../../../../assets/img/tl.png') no-repeat;
  background-size: 100% 100%;
}

.population-data b:nth-child(1) {
  top: 0;
  left: 0;
}

.population-data b:nth-child(2) {
  top: 0;
  right: 0;
  background-image: url('../../../../assets/img/tr.png');

}
.population-data b:nth-child(3) {
  bottom: 0;
  left: 0;
  background-image: url('../../../../assets/img/bl.png');

}
.population-data b:nth-child(4) {
  bottom: 0;
  right: 0;
  background-image: url('../../../../assets/img/br.png');
}
.box-zero {
  display: flex;
  margin-top: 1%;
  height: 13.6%;
}

.box-zero .population-total {
  display: flex;
  align-items: center;
}

.box-zero .num-total {
  display: flex;
  justify-content: space-between;
  width: 66%;
  height: 100%;
  margin-left: .15625rem;
}

.box-zero .num {
  width: 12%;
  background: url('../../../../assets/img/num_bg.png') no-repeat;
  background-size: 100% 100%;
  font-size: .195313rem;
  text-align: center;
}

.box-one {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-top: 5%;
}

.box-info {
  display: flex;
  height: 100%;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  font-size: .104167rem;
}

.box-info>p:nth-child(2) {
  margin-top: .019531rem;
  font-size: .078125rem;
}


.box-two {
  margin-top: 3%;
}

.box-two .box-two-border {
  margin-right: 4%;
}

.box-three {
  margin-top: 3%;
}

.box-three .box-three-border {
  margin-right: 4%;
}

.color-blue {
  color: #2691ff;
}

.color-green {
  color: #03fab3;
}

.color-yellow {
  color: #ffd200;
}
</style>