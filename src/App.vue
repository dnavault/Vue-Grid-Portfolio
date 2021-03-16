<template>
  <div id="app">
    <DataGrid
      :colHeaders="['ID', 'Name']"
      :rowData="[
        { id: 1, name: 'Test' },
        { id: 2, name: 'Test2' },
        { id: -1, name: 'Just Another Long Name' },
      ]"
    />
  </div>
</template>

<script>
import DataGrid from "./components/DataGrid";

export default {
  name: "App",

  components: {
    DataGrid,
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #2c3e50;
  margin-top: 60px;
}
</style>
