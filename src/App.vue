<template>
  <div id="app">
    <seve @tableData="assignData" />

    <table align="center" class="table table-bordered mt-5">
      <thead>
        <tr>
          <th>email</th>

          <th>id</th>

          <th>name</th>

          <th>status</th>
        </tr>

        <tr v-if="tableData.length > 0">
          <td>{{ tableData[0].email }}</td>

          <td>{{ tableData[0].id }}</td>

          <td>{{ tableData[0].name }}</td>

          <td>{{ tableData[0].status }}</td>
        </tr>
      </thead>

      <tbody></tbody>
    </table>
  </div>
</template>



<script>
import seve from "./components/seve.vue";

export default {
  name: "App",

  components: {
    seve,
  },

  data() {
    return {
      email: " ",

      id: "",

      name: " ",

      status: " ",

      tableData: [],
    };
  },

  methods: {
    assignData(data) {
      this.tableData = data;
    },
  },
};
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



