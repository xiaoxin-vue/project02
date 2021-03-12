<template>
  <div class="progress-demo">
    <span class="progress-text">{{proInfo.proText}}</span>
    <div class="content" :style="{width: proInfo.num + '%'}">
      <span class="num" :style="{marginLeft: (1.302083 * proInfo.num/100 - .097656) +'rem'}">{{proInfo.num}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProgressDemo',
  props: {
    proInfo: {
      type: Object,
      default() {
        return {
          num: 50,
          proText: ''
        }
      }
    }
  }
}
</script>

<style scoped>
.progress-demo {
  position: relative;
  width: 1.302083rem;
  height: .097656rem;
  background-color: #061c3a;
  border-radius: .045573rem;
}

.content {
  height: 100%;
  background: linear-gradient(90deg, #015DFF, #00C7FF);;
  border-radius: .045573rem;
}

.num {
  display: flex;
  align-content: center;
  font-size: .078125rem;
}

.progress-text {
  position: absolute;
  left: -0.3125rem;
  font-size: .078125rem;
  opacity: 0.5;
}
</style>