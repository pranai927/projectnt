<template>
  <div id="app">
    <!--img alt="Vue logo" src="./assets/logo.png" /-->
    
    <FormComponent />
    <TableComponent />
    <IdTable />

  </div>
</template>

<script>

import FormComponent from "./components/FormComponent.vue";
import TableComponent from "./components/TableComponent.vue";
import IdTable  from "./components/IdTable.vue";
export default {
  name: "App",
  components: {
   
    FormComponent,
     TableComponent,
     IdTable,
    
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
 
  color: #2c3e50;
  margin-top: 60px;
}
</style>
