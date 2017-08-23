<template>
<div class="add_user">

  <!-- form input to add content -->
  <form>

    <div class="form-group row">
      <label for="firstname" class="col-sm-3 col-md-2 col-lg-3 col-form-label">First Name</label>
      <div class="col-sm-9 col-md-10 col-lg-9">
        <input type="text" class="form-control" id="first_name" placeholder="first Name">
      </div>
    </div>

    <div class="form-group row">
      <label for="lastname" class="col-sm-3 col-md-2 col-lg-3 col-form-label">Last Name</label>
      <div class="col-sm-9 col-md-10 col-lg-9">
        <input type="text" class="form-control" id="last_name" placeholder="Last Name">
      </div>
    </div>

    <div class="form-group row">
      <label for="email" class="col-sm-3 col-md-2 col-lg-3 col-form-label">Email</label>
      <div class="col-sm-9 col-md-10 col-lg-9">
        <input type="email" class="form-control" id="_Email" placeholder="Email">
      </div>
    </div>

  <button type="submit" class="btn btn-primary">Submit</button>
</form>
<!-- -->

</div>
</template>

<script>

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@media screen and (min-width: 991px) {
    .add_user {
        margin-top: 55px;
    }
}
</style>
