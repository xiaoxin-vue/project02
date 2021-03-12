<template>
  <div class="efficiency">
    <b></b><b></b><b></b><b></b>
    <div class="eff-header">
      <span>效率值</span>
      <i></i>
    </div>
    <div class="eff-list">
      <eff-value :wrap="effVal87"/>
      <bar-chart/>
    </div>
  </div>
</template>

<script>
import BarChart from '../../../common/BarChart.vue'
import EffValue from '../../../common/EffValue.vue'

export default {
  name: 'Efficiency',
  data() {
    return {
      effVal87: {
        width: .781458, //140px -> .911458rem 
        height: .781458,
        value: [],
        clockDial: "#031428",
        scaleNum: 24,
        scaleWidth: .032552,
        scaleHeight: .097656,
        effValueNum: '87%',
        changeBgc: '#2691ff'
      }
    }
  },
  components: {
    EffValue,
    BarChart
  }
}
</script>

<style scoped>
.efficiency {
  position: relative;
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 24.6%;
  padding: 4%;
  background-color: #031428;
}

.efficiency b {
  display: inline-block;
  position: absolute;
  width: .104167rem;
  height: .104167rem;
  background: url('../../../../assets/img/tl.png') no-repeat;
  background-size: 100% 100%;
}

.efficiency b:nth-child(1) {
  top: 0;
  left: 0;
}

.efficiency b:nth-child(2) {
  top: 0;
  right: 0;
  background-image: url('../../../../assets/img/tr.png');

}
.efficiency b:nth-child(3) {
  bottom: 0;
  left: 0;
  background-image: url('../../../../assets/img/bl.png');

}
.efficiency b:nth-child(4) {
  bottom: 0;
  right: 0;
  background-image: url('../../../../assets/img/br.png');
}

.eff-header {
  display: flex;
}

.eff-header i {
  display: inline-block;
  width: 5%;
  height: 100%;
  margin-left: 3%;
  background: url('../../../../assets/img/help.png') no-repeat;
  background-size: 100% 100%;
}

.eff-list {
  margin-top: 2%;
  display: flex;
  flex: 1;
  align-items: center;
  justify-content: space-between;
}
</style>