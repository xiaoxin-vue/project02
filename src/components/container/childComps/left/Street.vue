<template>
  <div class="street">
    <span class="streetText">街道简介</span>
    <div class="streetInfo">
        <img src="../../../../assets/img/pic.png" alt="">
        <p>
          <span><i></i>南星街道，位于浙江省杭州市上城区境</span>
          <span>内。2005年，全街道面积4.31平方千米，人</span>
          <span>口3.86万人。代码330102008，居委会驻复</span>
          <span>兴路118号，邮编310008。辖8个社区。</span>
          <a href="#">查看更多>></a>
        </p>
    </div>
    <b class="bl"></b>
    <b class="br"></b>
  </div>
</template>

<script>
export default {
  name: 'Street'
}
</script>

<style scoped>
.street {
  position: relative;
  width: 100%;
  height: 20.7%;
  padding: 4%;
  padding-right: 1%;
  background:#031428  url('../../../../assets/img/box-tl.png') no-repeat;
  background-size: 100% .292969rem;
  clip-path: polygon(0 0, 90% 0, 100% .273438rem, 100% 100%,0 100%);
}

.streetInfo {
  margin-top: .065104rem;
}

.streetInfo img {
  float: left;
  width: 26%;
  height: 61%;
}

.streetInfo p {
  position: relative;
  float: left;
  margin-left: 4%;
  width: 69%;
  height: .696615rem;
  color: #fff;
  font-size: .078125rem;
}

.streetInfo span {
  display: block;
  height: 21%;
  line-height: .130208rem;
}

.streetInfo i {
  display: inline-block;
  width: .16276rem;
  height: .091146rem;
}

.streetInfo a {
  position: absolute;
  right: .23rem;
  bottom: -0.0531rem;
  border-bottom: .013021rem solid #019bcf;
  color: #019bcf;
  text-decoration: none;
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
</style>