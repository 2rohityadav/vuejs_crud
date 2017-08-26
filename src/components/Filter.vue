<template>
<div class="search">
{{ msg }}
  <!-- form input to add content -->
  <form>
  <div class="form-group">
    <input type="text" class="form-control" aria-describedby="search" placeholder="Search UserName...">
  </div>
</form>
<!-- -->

</div>
</template>

<script>
import { bus } from '../main'
export default {
  data () {
    return {
      msg: 'filter component'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@media screen and (max-width: 991px) {
    .search {
        margin-top: 50px;
    }
}
</style>
