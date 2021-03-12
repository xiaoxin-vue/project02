<template>
  <div class="manage-model">
    <b></b><b></b><b></b><b></b>
    <span class="task-text">管理模式<i></i></span>
    <div class="task-info">
      <div class="rotate1">
        <img src="../../../../assets/img/circle.png" alt="">
      </div>
      <div class="tasks">
        <div class="task-left1">
          <p>社区治理委员会</p>
        </div>
        <div class="task-right1">
          <p>
            <span>居委会</span>
            <span>物业公司</span>
            <span>业委会</span>
            <span>...</span>
          </p>
        </div>
      </div>
      <div class="rotate2">
        <img src="../../../../assets/img/circle.png" alt="">
      </div>
      <div class="tasks">
        <div class="task-left2">
          <p>公共服务站</p>
        </div>
        <div class="task-right2">
          <p>百通港：<span class="counterColor">64</span></p>
          <p>全科网格：<span class="counterColor">101</span></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ManageModel'
}
</script>

<style scoped>
.manage-model{
  position: relative;
  width: 100%;
  height: 18%;
  padding: 4% 0;
  background-color: #031428;
}

.manage-model b {
  display: inline-block;
  position: absolute;
  width: .104167rem;
  height: .104167rem;
  background: url('../../../../assets/img/tl.png') no-repeat;
  background-size: 100% 100%;
}

.manage-model b:nth-child(1) {
  top: 0;
  left: 0;
}

.manage-model b:nth-child(2) {
  top: 0;
  right: 0;
  background-image: url('../../../../assets/img/tr.png');

}
.manage-model b:nth-child(3) {
  bottom: 0;
  left: 0;
  background-image: url('../../../../assets/img/bl.png');

}
.manage-model b:nth-child(4) {
  bottom: 0;
  right: 0;
  background-image: url('../../../../assets/img/br.png');
}

.task-text {
  display: flex;
  align-items: center;
  padding-left: 4%;
}

.task-text i {
  display: inline-block;
  width: .104167rem;
  height: .104167rem;
  margin-left: .065104rem;
  background: url('../../../../assets/img/help.png') no-repeat;
  background-size: 100% 100%;
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

.task-left {
  position: absolute;
  top: .3125rem;
  left: .15625rem;
  font-size: .091146rem;
  font-weight: 600;
  text-align: center;
}

.task-left1 {
  width: 30%;
  position: absolute;
  top: 29%;
  left: 9%;
  text-align: center;
  z-index: 20;
}

.task-left1>p {
  margin-top: .052552rem;
  font-size: .078125rem;
}

.task-left2 {
  position: absolute;
  top: 41%;
  left: 9%;
  font-size: .078125rem;
  text-align: center;
  z-index: 20;
}

.task-right1 {
  position: absolute;
  top: 26%;
  right: 15%;
  font-size: .091146rem;
}

.task-right1 p span {
  display: block;
  line-height: .117656rem;
}

.task-right2 {
  position: absolute;
  top: 36%;
  right: 4%;
  font-size: .091146rem;
}

.task-right2>p:nth-child(2) {
  margin-top: 16%;
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