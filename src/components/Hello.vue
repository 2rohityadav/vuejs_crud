<template>
<div class="container">
  <h1>Hello VUE</h1>

  <!-- form input to add content -->
  <form>
  <div class="form-group">
    <label for="firstname">First Name</label>
    <input type="text" class="form-control" id="firstName" aria-describedby="firstname" placeholder="First Name">

    <label for="lastname">Last Name</label>
    <input type="text" class="form-control" id="lastName" aria-describedby="lastname" placeholder="Last Name">

    <label for="email">Email address</label>
    <input type="email" class="form-control" id="email" aria-describedby="email" placeholder="Enter email">
  </div>

  <button type="submit" class="btn btn-primary">Submit</button>
</form>
<!-- -->

  <hr>
  <table class="table mt-1h">
    <thead class="thead-inverse">
      <tr>
        <th>#</th>
        <th>First Name</th>
        <th>Last Name</th>
        <th>Username</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row">1</th>
        <td>Mark</td>
        <td>Otto</td>
        <td>@mdo</td>
      </tr>
      <tr>
        <th scope="row">2</th>
        <td>Jacob</td>
        <td>Thornton</td>
        <td>@fat</td>
      </tr>
      <tr>
        <th scope="row">3</th>
        <td>Larry</td>
        <td>the Bird</td>
        <td>@twitter</td>
      </tr>
    </tbody>
  </table>

</div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.mt-1h {
  margin-top: 100px;
}
</style>
