<template>
  <div class="wrap" ref="wrap" :style="{width: wrap.width + 'rem', height: wrap.height + 'rem', backgroundColor: wrap.clockDial}">
    <ul class="list">
      <li v-for="(item, index) in listArray" :key="index" 
          :style="{
          left: (wrap.width / 2 - .026042) + 'rem', 
          top: -.00651 + 'rem',
          transformOrigin: 'center ' + wrap.width / 2 + 'rem',
          borderRadius: wrap.scaleWidth / 2 + 'rem',
          width: wrap.scaleWidth + 'rem',
          height: wrap.scaleHeight + 'rem',
          transform: 'rotate(' + index * (360 /wrap.scaleNum) + 'deg)'
          }"
          :class="[{bgcAll: true} ,{active: index <= changeLiNum && wrap.changeBgc == '#2691ff'}, {active1: index <= changeLiNum && wrap.changeBgc == '#04cf99'}, {active2: index <= changeLiNum && wrap.changeBgc == '#ffd200'}]"></li>
    </ul>
    <span class="eff-num">{{wrap.effValueNum}}</span>
  </div>
</template>

<script>
export default {
  name: 'EffValue',
  data() {
    return {
      changeLiNum: 0
    }
  },
  props: {
    wrap: {
      type: Object,
      default() {
        return {
          width: .911458,
          height: .911458,
          value: [],
          clockDial: "#031428",
          scaleNum: 24,
          scaleWidth: .032552,
          scaleHeight: .097656,
          effValueNum: 50,
          changeBgc: 'red'
        }
      }
    }
  },
  created() {
  },
  mounted() {
    // 设置表盘的样式
    // this.$refs.wrap.style.width = this.wrap.width + 'px'
    // this.$refs.wrap.style.height = this.wrap.height + 'px'
    // this.$refs.wrap.style.backgroundColor = this.wrap.clockDial
    // 表盘刻度：获取dom上所有的li
    // let liList = document.querySelectorAll('li')
    // 给所有的li设置动态样式
    // for(let i = 0; i < this.wrap.scaleNum; i++) {
      /* 设置刻度相对位置值 left值 = width/2 - 1 */
      // liList[i].style.left = (this.wrap.width / 2 - 4) + 'px'
      // liList[i].style.top = -1 + 'px'
      // 刻度旋转中心点
      /* 用来设置元素的运动的基点（参照点）。默认点是元素的中心点 rotateY = height/2 */
      // liList[i].style.transformOrigin = 'center ' + this.wrap.width / 2 + 'px'
      // 刻度旋转角度
      // liList[i].style.transform = "rotate("+ (i * (360 /this.wrap.scaleNum) ) +"deg)"
      // 刻度背景
      // liList[i].style.background = this.wrap.scaleBgc
      // 刻度宽高边框
      // liList[i].style.width = this.wrap.scaleWidth + 'px'
      // liList[i].style.height = this.wrap.scaleHeight + 'px'
      // liList[i].style.borderRadius = this.wrap.scaleWidth / 2 + 'px'
    // }
    // 设置效率值
    let newNumStr =  this.wrap.effValueNum + ''
    let num = parseInt(newNumStr.substr(0, 2))
    this.changeLiNum = Math.floor(this.wrap.scaleNum * ( num / 100 ))
    // 根据效率值给刻度背景
    // for(let i = 0; i <= changeLi; i++) {
    //   liList[i].style.background = this.wrap.changeBgc
    // }
  },
  computed: {
    // 通过计算属性返回props中的value数组的长度,间接设置刻度的总数目
    listArray() {
      this.wrap.value.length = this.wrap.scaleNum
      return this.wrap.value
    }
  }
}
</script>

<style scoped>
.wrap{
  display: flex;
  position: relative;
  border-radius: 50%;
  align-items: center;
  justify-content: center;
  /* border: 1px solid red; */
}

li {
  position: absolute; 
  list-style: none;
}

.eff-num {
  font-size: .208333rem;
  color: #fff;
}

.bgcAll {
  background-color: #1d2c3e;
}

.active {
  background-color: #2691ff;
}

.active1 {
  background-color: #04cf99;
}

.active2 {
  background-color: #ffd200;
}
</style>