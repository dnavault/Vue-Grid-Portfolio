<template>
  <div>
    <div class="grid">
      <div v-for="col in colHeaders" :key="col">{{ col }}</div>
    </div>
    <div v-for="value in rowData" :key="value.id">
      <span v-for="item in value" :key="item">{{ item }}</span>
    </div>

    <table>
      <th class="colHeader" v-for="col in colHeaders" :key="col">
        {{ col }}
      </th>
      <tbody>
        <tr v-for="item in rowData" :key="item.id">
          <td class="tdGrid" v-for="value in item" :key="value">{{ value }}</td>
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
table {
  table-layout: fixed;
  width: 300px;
}
th {
  text-align: left;
}

.grid {
  display: grid;
  grid-template-columns: 120px 500px;
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
  width: 25%;
}
</style>
