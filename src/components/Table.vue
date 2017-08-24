<template>
<div>
  <table class="table mt-1h">
    <thead class="thead-inverse">
      <tr>
        <th>#</th>
        <th>First Name</th>
        <th>Last Name</th>
        <th>Username</th>
        <th></th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="user in users">
        <th scope="row">1</th>
        <td>{{ user.firstname }}</td>
        <td>{{ user.lastname }}</td>
        <td>{{ user.email }}</td>
        <td>
          <button type="button" class="btn btn-outline-info btn-sm">Edit</button>
          <button type="button" class="btn btn-outline-danger btn-sm">Delete</button>
        </td>
      </tr>
      <!-- <tr>
        <th scope="row">2</th>
        <td>Jacob</td>
        <td>Thornton</td>
        <td>@fat</td>
        <td>
          <button type="button" class="btn btn-outline-info btn-sm">Edit</button>
          <button type="button" class="btn btn-outline-danger btn-sm">Delete</button>
        </td>
      </tr>
      <tr>
        <th scope="row">3</th>
        <td>Larry</td>
        <td>the Bird</td>
        <td>@twitter</td>
        <td>
          <button type="button" class="btn btn-outline-info btn-sm">Edit</button>
          <button type="button" class="btn btn-outline-danger btn-sm">Delete</button>
        </td>
      </tr> -->
    </tbody>
  </table>

</div>
</template>
<script>

export default {
  props: ['users']
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@media screen and (max-width: 991px) {
    .table {
        margin-top: 30px;
    }
}
</style>
