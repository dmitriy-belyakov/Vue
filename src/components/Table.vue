<template>
    <div id = "table">
        <el-table
            :data="Data">
            <el-table-column
                label = "Name"
                prop = "name">
            </el-table-column>
            <el-table-column
                label = "Age"
                prop = "age">
            </el-table-column>
            <el-table-column
                label = "Sex"
                prop = "sex">
            </el-table-column>
            <el-table-column
                align="right">
                <el-button
                    size="mini"
                    @click="Edit()">Edit
                </el-button>
                <el-button
                    size="mini"
                    type="danger"
                    @click="Delete()">Delete
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
      Data: [
        {
          name: 'John',
          age: 18,
          sex: 'Male'
        },
        {
          name: 'Ann',
          age: 17,
          sex: 'Female'
        },
        {
          name: 'Kate',
          age: 21,
          sex: 'Female'
        },
        {
          name: 'Sam',
          age: 19,
          sex: 'Male'
        }
      ]
    }
  },
  methods: {
    Edit () {
      alert('NOT YET!')
    },
    Delete () {
      this.delete()
    }
  }
}
</script>

<style scoped>
    @import url("//unpkg.com/element-ui@2.12.0/lib/theme-chalk/index.css");

    #table{
        width: 75%;
        height: 100%;
        margin-top: 5%;
        margin-left: 5%;
        float: left;
    }
</style>
