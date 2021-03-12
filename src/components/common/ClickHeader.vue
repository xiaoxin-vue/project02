<template>
  <div class="click-header">
    <span v-for="(item, index) in textArray" @click="itemClick(index)" class="item" :class="{active: index === currentIndex}">{{item}}</span>
  </div>
</template>

<script>
export default {
  name: 'ClickHeader',
  data() {
    return {
      currentIndex: 0
    }
  },
  props: {
    textArray: {
      type: Array,
      defautl() {
        return []
      }
    }
  },
  methods: {
    itemClick(index) {
      this.currentIndex = index
    }
  }
}
</script>

<style scoped>
.click-header {
  position: relative;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding-bottom: .019531rem;
  width: 100%;
  height: .360625rem;
  z-index: 11;
}

.item {
  width: .651042rem;
  height: .260417rem;
  line-height: .260417rem;
  text-align: center;
  opacity: 0.5;
  cursor: pointer;
}

.active {
  opacity: 1;
  color: #fff;
  background: url('../../assets/img/btn.png') no-repeat;
  background-size: 100% 100%;
}
</style>