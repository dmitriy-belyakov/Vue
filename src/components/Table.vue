<template>
  <div class="table">
    <el-input
      v-model="search"
      size="mini"
      type="string"
      placeholder="Type to Search"
    />
    <br>
    <el-table
      :data="filteredDataset"
    >
      <el-table-column
        label="Name"
        prop="name"
      />
      <el-table-column
        label="Age"
        prop="age"
      />
      <el-table-column
        label="Gender"
        prop="gender"
      />
      <el-table-column
        align="right">
        <el-button
          size="mini"
          @click="edit"
        >
          Edit
        </el-button>
        <el-button
          size="mini"
          type="danger"
          @click="del"
        >
          Delete
        </el-button>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: 'table',
  data () {
    return {
      dataset: [
        {
          name: 'John',
          age: 18,
          gender: 'Male'
        },
        {
          name: 'Ann',
          age: 17,
          gender: 'Female'
        },
        {
          name: 'Kate',
          age: 21,
          gender: 'Female'
        },
        {
          name: 'Sam',
          age: 19,
          gender: 'Male'
        },
        {
          name: 'Alex',
          age: 29,
          gender: 'Male'
        }
      ],
      search: ''
    }
  },
  methods: {
    edit () {
      alert('NOT YET!')
    },
    del () {
      alert('NOT YET!')
    }
  },
  computed: {
    filteredDataset () {
      return this.dataset.filter(data =>
        !this.search || data.name.toLowerCase().includes(this.search.toLowerCase())
      )
    }
  }
}
</script>

<style scoped>
    @import url("//unpkg.com/element-ui@2.12.0/lib/theme-chalk/index.css");

    .table{
        width: 75%;
        height: 100%;
        margin-top: 5%;
        margin-left: 5%;
        float: left;
        margin-right: 0;
        margin-bottom: 1%;
        padding: 0;
    }

    .el-input{
      width: 40vh;
      float: right;
    }
</style>
