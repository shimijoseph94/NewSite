<template>
<div>
<div style="margin-top:50px; padding-bottom:40px;padding-top:30px;">
   <h4 style="text-align:center; color:#f6142a;">Drop nail a line</h4>
  </div>
   <div style="width:800px; margin:0 auto;"> 
  <form>
    <div class="form-group">
      <label for="email">Email:</label>
      <input type="email" class="form-control" id="email" placeholder="Enter email" name="email">
    </div>
    <div class="form-group">
      <label for="pwd">Password:</label>
      <input type="password" class="form-control" id="pwd" placeholder="Enter password" name="pswd">
    </div>
    <div class="form-group form-check">
      <label class="form-check-label">
        <input class="form-check-input" type="checkbox" name="remember"> Remember me
      </label>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
  <br>
  </div>
</div>

</template>
<script>
export default {
  name: 'Contact',
  data () {
   }
}

</script>
<style>

<style>