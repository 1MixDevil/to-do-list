<template>
  <div id="app">
    <SearchInfo @add-search="serchInfo"></SearchInfo>
    <FormAddToDo @new-info="addNewList"></FormAddToDo>
    <PrintTable @new-info="correctionInfo" :full-info="toDo" :search="search"> </PrintTable>
  </div>
</template>

<script>

import FormAddToDo from "@/components/FormAddToDo";
import PrintTable from "@/components/PrintTable";
import SearchInfo from "@/components/SearchInfo";
export default {
  name: 'App',
  components: {
    SearchInfo,
    PrintTable,
    FormAddToDo

  },
  data(){
    return{
      toDo: [],
      search: "",
    }
  },
  methods: {
    addNewList(text){
      this.toDo.unshift(text)
    },
    correctionInfo(newInfo){
      this.toDo = newInfo
    },
    serchInfo(text){
      this.search=text;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
