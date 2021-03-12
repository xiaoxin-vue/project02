<template>
  <div ref="two" class="box-border" :style="{ width: boxStyle.width + 'rem', height: boxStyle.height + 'rem' }">
    <b class="border-b" :style="{borderColor: boxStyle.borderColor}" :class="{active: boxStyle.bgColor === '#031428'}"></b>
    <b class="border-b" :style="{borderColor: boxStyle.borderColor}" :class="{active: boxStyle.bgColor === '#031428'}"></b>
    <b class="border-b" :style="{borderColor: boxStyle.borderColor}" :class="{active: boxStyle.bgColor === '#031428'}"></b>
    <b class="border-b" :style="{borderColor: boxStyle.borderColor}" :class="{active: boxStyle.bgColor === '#031428'}"></b>
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BoxBorder',
  props: {
    boxStyle: {
      type: Object,
      default() {
        return {
          width: 108,
          height: 76,
          BborderColor: '#2691ff'
        }
      }
    }
  }
}
</script>

<style scoped>
.box-border {
  display: inline-block;
  position: relative;
  background-color:#061C3A;
}

.box-border b {
  position: absolute;
  display: inline-block;
  width: .091146rem;
  height: .091146rem;
  background: #061C3A;
  border: 1px solid;
}

.box-border b:nth-child(1) {
  border-bottom: 0;
  border-right: 0;
}

.box-border b:nth-child(2) {
  top: 0;
  right: 0;
  border-left: 0;
  border-bottom: 0;
}
.box-border b:nth-child(3) {
  bottom: 0;
  left: 0;
  border-right: 0;
  border-top: 0;
}
.box-border b:nth-child(4) {
  bottom: 0;
  right: 0;
  border-left: 0;
  border-top: 0;
}

.content {
  height: 100%;
}

.box-border .active {
  background-color: #031428;
}
</style>