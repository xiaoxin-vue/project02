<template>
  <div class="MoodIndex">
    <b class="bl"></b>
    <b class="br"></b>
    <div class="content">
      <eff-value :wrap="effVal92"/>
      <eff-value :wrap="effVal75"/>
      <span class="mood-text">社工心情指数<em></em></span>
      <span class="satisfaction-text">群众满意度<em></em></span>
    </div>
  </div>
</template>

<script>
import EffValue from '../../../common/EffValue.vue'
export default {
  components: { EffValue },
  name: 'MoodIndex',
  data() {
    return {
      effVal92: {
        width: .781458, 
        height: .781458,
        value: [],
        clockDial: "#031428",
        scaleNum: 24,
        scaleWidth: .032552,
        scaleHeight: .097656,
        effValueNum: 92,
        changeBgc: '#2691ff'
      },
      effVal75: {
        width: .781458,
        height: .781458,
        value: [],
        clockDial: "#031428",
        scaleNum: 24,
        scaleWidth: .032552,
        scaleHeight: .097656,
        effValueNum: 75,
        changeBgc: '#04cf99'
      }
    }
  },
}
</script>

<style scoped>
.MoodIndex {
  position: relative;
  width: 100%;
  height: 20.7%;
  padding: 4%;
  padding-top: 0;
  background: #031428 url('../../../../assets/img/box-tr.png') no-repeat;
  background-size: 100% .292969rem;
  clip-path: polygon(10% 0, 100% 0, 100% 100%, 0 100%, 0 .273438rem);
}

.br,
.bl {
  display: inline-block;
  width: .104167rem;
  height: .091146rem;
  position: absolute;
  bottom: 0;
}

.br {
  right: 0;
  background: url('../../../../assets/img/br.png') no-repeat;
  background-size: 100% 100%;
}

.bl {
  left: 0;
  background: url('../../../../assets/img/bl.png') no-repeat;
  background-size: 100% 100%;
}

.content {
  display: flex;
  position: relative;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  height: 100%;
}

.mood-text,
.satisfaction-text {
  display: flex;
  align-items: center;
  color: #fff;
  font-weight: 700;
  font-size: .091146rem;
}

.mood-text {
  position: absolute;
  bottom: -0.019531rem;
  left: .305521rem;
}

.satisfaction-text {
  position: absolute;
  bottom: -0.019531rem;
  right: 10%;
}

.content em {
  display: inline-block;
  width: .104167rem;
  height: .104167rem;
  margin-left: .065104rem;
  background: url('../../../../assets/img/help.png') no-repeat;
  background-size: 100% 100%;
}
</style>