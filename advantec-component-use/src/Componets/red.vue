<template>
  <div>
 <div class="row">
   <slot name="redComp"></slot>
 </div>
  </div>
</template>
<script>
export default {

};
</script>
<style scoped>
div.row{
  height: 70px;
  background-color: red;
}
</style>
