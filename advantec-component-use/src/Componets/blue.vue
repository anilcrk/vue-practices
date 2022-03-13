<template>
  <div>
 <div class="row">
   <slot name="blueComp"></slot>
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
  background-color: blue;
}
</style>
