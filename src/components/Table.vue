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
    </tbody>
  </table>

</div>
</template>
<script>
import { bus } from '../main'
export default {
  data() {
    return {
      users: [
        {firstname: 'Rohit', lastname: 'Yadav', email: '@rohit'},
        {firstname: 'Nitin', lastname: 'Deni', email: '@nitin'},
        {firstname: 'Sanjay', lastname: 'Saar', email: '@sanjay'}
      ],
      msg: 'table component'
    }
  },
  // recieving bus event
  created () {
    bus.$on('emmitingUser', (data) => {
      console.log(data);
      this.users.push({
        firstname: data.firstName,
        lastname: data.firstName,
        email: data.email
      });
      data.firstName = "";
      data.lastName = "";
      data.email = "";
    })
  }
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
