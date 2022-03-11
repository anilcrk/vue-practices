<template>
<div>
  <p class="text-center">{{content}}</p>
  </div>
</template>
<script>
export default{
  props : ["content"]
}
</script>

<style scoped> /* scoped --> sadece bu component de kullanıcak ise yazılır.*/
  div {
    border : 1px solid #cddd;
    box-shadow: 1px 1px 2px #666;
    padding: 20px 20px;
    margin-top: 20px ;
  }
</style>
