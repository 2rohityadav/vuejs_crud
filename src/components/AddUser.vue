<template>
<div class="add_user">
  <br>
  <!-- form input to add content -->
  <form>

    <div class="form-group row">
      <label for="firstname" class="col-sm-3 col-md-2 col-lg-3 col-form-label">First Name</label>
      <div class="col-sm-9 col-md-10 col-lg-9">
        <input type="text" class="form-control" placeholder="first Name" v-model="newUsers.firstName">
      </div>
    </div>

    <div class="form-group row">
      <label for="lastname" class="col-sm-3 col-md-2 col-lg-3 col-form-label">Last Name</label>
      <div class="col-sm-9 col-md-10 col-lg-9">
        <input type="text" class="form-control" placeholder="Last Name" v-model="newUsers.lastName">
      </div>
    </div>

    <div class="form-group row">
      <label for="email" class="col-sm-3 col-md-2 col-lg-3 col-form-label">Email</label>
      <div class="col-sm-9 col-md-10 col-lg-9">
        <input type="email" class="form-control" placeholder="Email" v-model="newUsers.email">
      </div>
    </div>

  <button type="button" class="btn btn-primary" @click="addUser()">Submit</button>
</form>
<!-- -->

</div>
</template>

<script>
import { bus } from '../main'
export default {
  data () {
    return {
      msg: 'add user components',
      newUsers: {
        firstName: '',
        lastName: '',
        email: ''
      }
    }
  },
  methods: {
    addUser () {
      bus.$emit('emmitingUser', this.newUsers)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@media screen and (min-width: 991px) {
    .add_user {
        margin-top: 55px;
    }
}
</style>
