<template>
  <div>
    <table>
      <th class="colHeader" v-for="col in colHeaders" :key="col">
        {{ col }}
      </th>
      <tbody>
        <tr v-for="value in rowData" :key="value.id">
          <td class="tdGrid" v-for="item in value" :key="item">{{ item }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "DataGrid",
  props: {
    colHeaders: Array,
    rowData: Array,
  },
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

.colHeaders {
  display: flex;
}

.colHeader {
  margin-left: 20px;
}

.rows {
  display: flex;
}

.row {
  display: flex;
  margin-right: 20px;
}

.tdGrid {
  text-align: left;
}
</style>
