<template>
  <div>
 <h1>NewMemory Component</h1>
 <button @click="counter++">Arttır</button>
 <button @click="counter--">Azalt</button>
 <p>counter : {{counter}}</p>
  </div>
</template>
<script>
export default {
data:function(){
  return {counter : 0,};
}
};
</script>
