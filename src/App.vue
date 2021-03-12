<template>
  <div class="wrapper">
    <header-info/>
    <container/>
  </div>
</template>

<script>
import HeaderInfo from './components/headerInfo/HeaderInfo'
import Container from './components/container/Container'

export default {
  name: 'App',
  components: {
    HeaderInfo,
    Container
  }
}
</script>

<style scoped>
@import "./assets/css/normalize.css";

.wrapper {
  padding: .065rem;
  width: 100%;
  height: 6.627604rem;
  background-color: #000912;
  font-size: .104167rem;
  color: #fff;
}

</style>
