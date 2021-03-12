<template>
  <div class="task-data">
    <b></b><b></b><b></b><b></b>
    <span class="task-text">任务数据</span>
    <div class="task-info">
      <div class="rotate1">
        <img src="../../../../assets/img/circle.png" alt="">
      </div>
      <div class="tasks">
        <div class="task-left1">
          <span class="counterColor">2000</span>
          <p>总任务</p>
        </div>
        <div class="task-right">
          <p>进行中：<span class="counterColor">300</span></p>
          <p>已办结：<span class="counterColor">1700</span></p>
        </div>
      </div>
      <div class="rotate2">
        <img src="../../../../assets/img/circle.png" alt="">
      </div>
      <div class="tasks">
        <div class="task-left2">
          <span class="counterColor">200</span>
          <p>今日任务</p>
        </div>
        <div class="task-right">
          <p>进行中：<span class="counterColor">50</span></p>
          <p>已办结：<span class="counterColor">150</span></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TaskData'
}
</script>

<style scoped>
.task-data {
  position: relative;
  width: 100%;
  height: 18%;
  padding: 4% 0;
  background-color: #031428;
}

.task-data b {
  display: inline-block;
  position: absolute;
  width: .104167rem;
  height: .104167rem;
  background: url('../../../../assets/img/tl.png') no-repeat;
  background-size: 100% 100%;
}

.task-data b:nth-child(1) {
  top: 0;
  left: 0;
}

.task-data b:nth-child(2) {
  top: 0;
  right: 0;
  background-image: url('../../../../assets/img/tr.png');

}
.task-data b:nth-child(3) {
  bottom: 0;
  left: 0;
  background-image: url("../../../../assets/img/bl.png");

}
.task-data b:nth-child(4) {
  bottom: 0;
  right: 0;
  background-image: url('../../../../assets/img/br.png');
}

.task-text {
  padding-left: 4%;
}

.task-info {
  width: 100%;
  height: 78%;
  margin-top: 1%;
}


.tasks {
  float: left;
  position: relative;
  width: 49%;
  height: .663216rem;
  background: url('../../../../assets/img/box_bg.png') no-repeat;
  background-size: 100% 100%;
}

.tasks:nth-child(1) {
  margin-right: .050083rem;
}

.task-left1 {
  position: absolute;
  top: 31%;
  left: 15%;
  font-size: .091146rem;
  text-align: center;
  z-index: 20;
}

.task-left1>p {
  margin-top: .032552rem;
  font-size: .078125rem;
}

.task-left2 {
  position: absolute;
  top: 31%;
  left: 12%;
  font-size: .091146rem;
  text-align: center;
  z-index: 20;
}

.task-left2>p {
  margin-top: .032552rem;
  font-size: .078125rem;
}

.task-right {
  position: absolute;
  top: 36%;
  right: 8%;
  font-size: .091146rem;
}

.task-right>p:nth-child(2) {
  margin-top: 20%;
}

.counterColor {
  color: #ffd200;
}


.rotate1 {
  position: absolute;
  width: .592448rem;
  height: .605479rem;
  z-index: 14;
  top: .273438rem;
  left: .013021rem;
  animation: rotate1 4s linear infinite;
}

.rotate1 img{
  width: 100%;
  height: 100%;
}

@keyframes rotate1{
	0%{
		transform: rotateZ(0deg);/*从0度开始*/
	}
	100%{
		transform: rotateZ(360deg);/*360度结束*/
	}
}

.rotate2 {
  position: absolute;
  width: .585938rem;
  height: .592448rem;
  z-index: 14;
  top: .286458rem;
  right: .751302rem;
  animation: rotate1 4s linear infinite;
}

.rotate2 img {
  width: 100%;
  height: 100%;
}

</style>