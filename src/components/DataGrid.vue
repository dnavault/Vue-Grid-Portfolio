<template>
 <div>
    <ul>
      <li v-for="col in colHeaders" :key="col">{{ col }}</li>
    </ul>
    <ul>
      <li style="display:block" v-for="row in rowData" :key="row.id">{{ row.id }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "DataGrid",
  props: {
    colHeaders: Array,
    rowData: Array
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
