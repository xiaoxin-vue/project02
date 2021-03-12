<template>
  <div class="StreetMap">
    <b></b><b></b><b></b><b></b>
    <span class="map-text">街道地图</span>
    <div class="map">
      <div class="map-common map-add1">
        <p>白塔岭社区</p>
        <img src="../../../../assets/img/map_icon.png" alt="">
        <i></i>
      </div>
      <div class="map-common map-add2">
        <p>水澄桥社区</p>
        <img src="../../../../assets/img/map_icon.png" alt="">
        <i></i>
      </div>
      <div class="map-common map-add3">
        <p>海月桥社区</p>
        <img src="../../../../assets/img/map_icon.png" alt="">
        <i></i>
      </div>
      <div class="map-common map-add4">
        <p>复兴街社区</p>
        <img src="../../../../assets/img/map_icon.png" alt="">
        <i></i>
      </div>
      <div class="map-common map-add5">
        <p>美政桥社区</p>
        <img src="../../../../assets/img/map_icon.png" alt="">
        <i></i>
      </div>
      <div class="map-common map-add6">
        <p>玉皇山社区</p>
        <img src="../../../../assets/img/map_icon.png" alt="">
        <i></i>
      </div>
      <div class="map-common map-add7">
        <p>馒头山社区</p>
        <img src="../../../../assets/img/map_icon.png" alt="">
        <i></i>
      </div>
      <div class="map-common map-add8">
        <p>紫花埠社区</p>
        <img src="../../../../assets/img/map_icon.png" alt="">
        <i></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StreetMap'
}
</script>

<style scoped>
.StreetMap { 
  position: relative;
  width: 100%;
  height: 33.8%;
  padding: 2%;
  background-color: #031428;
  background-size: contain;
}
.StreetMap b {
  display: inline-block;
  position: absolute;
  width: .104167rem;
  height: .104167rem;
  background: url('../../../../assets/img/tl.png') no-repeat;
  background-size: 100% 100%;
}

.StreetMap b:nth-child(1) {
  top: 0;
  left: 0;
}

.StreetMap b:nth-child(2) {
  top: 0;
  right: 0;
  background-image: url('../../../../assets/img/tr.png');

}
.StreetMap b:nth-child(3) {
  bottom: 0;
  left: 0;
  background-image: url('../../../../assets/img/bl.png');

}
.StreetMap b:nth-child(4) {
  bottom: 0;
  right: 0;
  background-image: url('../../../../assets/img/br.png');
}

.map {
  position: relative;
  width: 100%;
  height: 84%;
  margin-top: 2%;
  background: url('../../../../assets/img/map.png') no-repeat;
  background-size: 100% 100%;
}

.map .map-common {
  width: .50073rem;
  height: .3rem;
  position: absolute;
  text-align: center;
  /* transform: scale(0.7); */
  animation: translation1 2s linear infinite;
}

.map-common i {
  position: relative;
  display: block;
  width: 80%;
  height: 90%;
  background: url('../../../../assets/img/triangle.svg') no-repeat;
  background-size: 100% 100%;
  transform: rotateX(61deg);
  left: 10%;
  top: -53%;
}

@keyframes translation1{
	0%{
		transform: translate(0, 0);/*从0度开始*/
	}
	50%{
		transform: translate(0, .065104rem);/*360度结束*/
	}
  100%{
		transform: translate(0, 0);/*360度结束*/
	}
}

.map-common>p {
  font-size: .078125rem;
  text-shadow: 1px 1px 0px rgba(0, 29, 62, 0.4);
  opacity: 0.8;
}

.map-common img {
  width: 45%;
  height: 100%;
}

.map-add1 {
  left: 12%;
  top: 48%;
}
.map-add2 {
  left: 36%;
  bottom: 22%;
}
.map-add3 {
  left: 53%;
  top: 49%;
}
.map-add4 {
  right: 27%;
  bottom: 52%;
}
.map-add5 {
  right: 16%;
  bottom: 45%;
}
.map-add6 {
  left: 31%;
  top: 14%;
}
.map-add7 {
  right: 26%;
  top: -4%;
}
.map-add8 {
  right: 9%;
  bottom: 56%;
}
</style>