<template>
  <div class="gear">
    <div class="rotate" :class="{antiWise: gearData.clockWise}">
      <img src="../../assets/img/gear.png" alt="">
    </div>
    <span class="gearText">{{gearData.text}}</span>
  </div>
</template>

<script>
export default {
  name: 'Gear',
  props: {
    gearData: {
      type: Object,
      default() {
        return {
          text: '',
          clockWise: true
        } 
      }
    }
  }
}
</script>

<style scoped>
.gear {
  position: relative;
  width: .885417rem;
  height: .885417rem;
}
.gear .rotate {
  animation: rotate 6s linear infinite;
}

.gear .antiWise {
  animation: rotate1 6s linear infinite;
}

.gear img {
  width: 100%;
  height: 100%;
}

@keyframes rotate{
	0%{
		transform: rotateZ(0deg);/*从0度开始*/
	}
	100%{
		transform: rotateZ(360deg);/*360度结束*/
	}
}

@keyframes rotate1{
	0%{
		transform: rotateZ(0deg);/*从0度开始*/
	}
	100%{
		transform: rotateZ(-360deg);/*360度结束*/
	}
}

.rotate:hover {
  animation-play-state: paused;
}

.gearText {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #fff;
}
</style>