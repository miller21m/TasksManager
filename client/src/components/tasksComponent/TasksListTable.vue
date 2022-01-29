<template>
<!-- This components sotres all the records of the tasks then we are looping all the tasks and retunring a single record -->
  <div class="m_TasksTable">
    <v-row>
      <v-col class="m_headerLabel" xs="5" sm="5" md="5">Name</v-col>
      <v-col class="m_headerLabel" xs="2" sm="2" md="2">Status</v-col>
      <v-col class="m_headerLabel" xs="4" sm="4" md="4">Assign</v-col>
      <v-col class="m_headerLabel" xs="1" sm="1" md="1"></v-col>
    </v-row>

    <div v-for="task in tasksList" :key="task.id">
      <app-row :taskData="task"/>
    </div>
  </div>
</template>


<script>
import Row from './Task.vue';
export default {
  props:['tasksList'],
  components:{
    appRow:Row
  }
  
}
</script>


<style scoped>
.m_TasksTable{
  margin:0px 20px;
  text-align: left;
  width: 90%;

}

.m_headerLabel{
  color: #676879;
}

</style>