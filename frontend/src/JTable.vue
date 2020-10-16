<template>
  <table>
    <tr>
      <th v-for="header in headers">{{header}}</th>
    </tr>
    <tr v-for="row in values">
      <td v-for="col of row">
        <input :value="col" />
      </td>
    </tr>
  </table>
</template>
<script>
export default {
  name: "JTable",
  props: {
    headers: Array,
    values: Array
  }
};
</script>
<style scoped>
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

th {
  color: white;
  height: 40px;
  background-color: #55aced;
  padding: 4px;
  text-align: center;
  border: 1px solid white;
}

td {
  height: 40px;
  background-color: #dddddd;
  border: 1px solid white;
}

td input {
  background-color: #dddddd;
  border: none;
  font-size: 16px;
}
</style>