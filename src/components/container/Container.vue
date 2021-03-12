<template>
  <div class="container">
    <div class="left">
      <street/>
      <task-data class="item"/>
      <population-data class="item"/>
      <efficiency class="item"/>
    </div>
    <div class="content">
      <main-plate/>
      <street-map class="item2"/>
      <final-plate class="item2"/>
    </div>
    <div class="right">
      <mood-index/>
      <manage-model class="item"/>
      <personnel class="item"/>
      <data-integrity class="item"/>
    </div>
  </div>
</template>

<script>
import Street from './childComps/left/Street.vue'
import TaskData from './childComps/left/TaskData.vue'
import PopulationData from './childComps/left/PopulationData.vue'
import Efficiency from './childComps/left/Efficiency.vue'
import MoodIndex from './childComps/right/MoodIndex.vue'
import ManageModel from './childComps/right/ManageModel.vue'
import Personnel from './childComps/right/Personnel.vue'
import DataIntegrity from './childComps/right/DataIntegrity.vue'
import MainPlate from './childComps/content/MainPlate.vue'
import StreetMap from './childComps/content/StreetMap.vue'
import FinalPlate from './childComps/content/FinalPlate.vue'

export default {
  name: 'Container',
  components: {
    Street,
    TaskData,
    PopulationData,
    Efficiency,
    MoodIndex,
    ManageModel,
    Personnel,
    DataIntegrity,
    MainPlate,
    StreetMap,
    FinalPlate
  }
}
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-between; 
  height: 6rem; 
}

.left,
.right {
  width: 27%;
  padding: 0.6% 0 0 0;
}

.content {
  flex: 1;
  /* background-color: #000b17; */
  padding: 0 0.6%;
}

.item {
  margin-top: 2%;
}

.item2 {
  margin-top: 1.2%;
}
</style>