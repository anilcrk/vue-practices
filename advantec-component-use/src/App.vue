<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <app-memory>
            <h1>Güzek bir gün</h1>
            <p>Bu gün hava karlı ve oldukça soğuk</p>
        </app-memory>
      </div>
    </div>
  </div>
</template>

<script>
import Memory from "./Memory.vue";


export default {
components : {
  appMemory : Memory
  }
}

</script>

