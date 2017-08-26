<template>
<div class="container">

  <h1>{{title}}</h1>
  <hr>
  <br>

  <div class="row">
    <div class="col-lg-6">
      <add-user></add-user>
    </div>

    <div class="col-lg-6">
      <div class="mr-auto">
        <app-filter></app-filter>
        <appTable></appTable>
      </div>
    </div>
  </div>

</div>
</template>

<script>
import Filter from './Filter'
import AddUser from './AddUser'
import Table from './Table'

export default {
  components: {
    'AppFilter': Filter,
    'addUser': AddUser,
    'appTable': Table
  },
  name: 'hello',
  data() {
    return {
      title: 'Vuejs 2.0 - CRUD'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .f_ryt{
    float: right;
  }
</style>
