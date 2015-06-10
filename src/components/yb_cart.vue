<style>
.green {
  color: green;
}
</style>

<template>
  <h2 class="green">{{msg}}</h2>
  <h2 class="green">This is coming from a static parameter passed directly to the component: {{custom}}</h2>
  <h2 class="green">This is coming from a dynamic parameter passed directly to the component: {{dynamic}}</h2>
</template>

<script>
module.exports = {
  props: ["custom","dynamic"],
  data: function () {
    return {
      msg: 'Hello from Cart!'
    }
  }
}
</script>