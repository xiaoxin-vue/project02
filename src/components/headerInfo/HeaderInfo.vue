<template>
  <div class="header-info">
    <div class="left">
      <div class="position">
        <i></i>
        <i></i>
        <i></i>
        <i></i>
        <em id="em1"></em>
        <em id="em2"></em>
        <em id='em3'></em>
        <em id="em4"></em>
        <span>南星街道<b></b></span> 
      </div>
    </div>
    <div class="center">
      <span>数字化精益管理平台</span>
    </div>
    <div class="right">
      <span>15:30:27</span>
      <span class="date">2019年8月13日</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderInfo'
}
</script>

<style scoped>
.header-info {
  position: relative;
  display: flex;
  align-items: center;
  height: .505208rem;
  border-bottom: 1px solid #00458a;
}

.center {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 26%;
  height: .563385rem;
  background: url('../../assets/img/heard_bg.png') no-repeat;
  background-size: 100% 100%;
}

.center span {
  color: #fff;
  font-size: .195313rem;
  font-weight: 700;
  letter-spacing: .058594rem
}

.left,
.right {
  width: 37%;
}

.position {
  position: relative;
  width: .864583rem;
  height: .325521rem;
  line-height: .325521rem;
  border: 1px solid #00458a;
  color: #fff;
}

.position i {
  display: inline-block;
  position: absolute;
  width: .104167rem;
  height: .104167rem;
}

.position i:nth-child(1) {
  top: -0.013021rem;
  left: -0.013021rem;
  border-left: .013021rem solid #00aaff;
  border-top: .013021rem solid #00aaff;
}

.position i:nth-child(2) {
  top: -0.013021rem;
  right: -0.013021rem;
  border-right: .013021rem solid #00aaff;
  border-top: .013021rem solid #00aaff;
}

.position i:nth-child(3) {
  bottom: -0.013021rem;
  left: -0.013021rem;
  border-bottom: .013021rem solid #00aaff;
  border-left: .013021rem solid #00aaff;
}

.position i:nth-child(4) {
  bottom: -0.013021rem;
  right: -0.013021rem;
  border-right: .013021rem solid #00aaff;
  border-bottom: .013021rem solid #00aaff;
}

.position span {
  margin-left: .065104rem;
}

.position em {
  display: inline-block;
  position: absolute;
  width: .052083rem;
  height: .052083rem;
  z-index: 10;
  border: 1px solid #00458a;
}


.position #em1 {
  left: .052083rem;
  top: .052083rem;
  border-right: 0;
  border-bottom: 0;
}

.position #em2 {
  right: .052083rem;
  top: .052083rem;
  border-bottom: 0;
  border-left: 0;
}

.position #em3 {
  bottom: .052083rem;
  left: .052083rem;
  border-right: 0;
  border-top: 0;
}

.position #em4 {
  bottom: .052083rem;
  right: .052083rem;
  border-left: 0;
  border-top: 0;
}


span b {
  position: absolute;
  right: .130208rem;
  top: .123698rem;
  display: inline-block;
  width: .052083rem;
  height: .052083rem;
  border: 1px solid #fff;
  border-left: 0;
  border-bottom: 0;
  transform: rotate(135deg);
}

.right {
  color: #fff;
  font-size: .078125rem;
}

.right span {
  float: right;
}

.date {
  margin-right: .260417rem;
}
</style>