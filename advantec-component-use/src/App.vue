<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <br />
        <br />
        <button
          @click="selectedComponent = 'appMemory'"
          class="btn-sm btn btn-primary"
        >
          appMemory
        </button>
        <button
          @click="selectedComponent = 'appNewMomory'"
          class="btn-sm btn btn-warning"
        >
          appNewMemory
        </button>
        <button
          @click="selectedComponent = 'appAuthor'"
          class="btn-sm btn btn-danger"
        >
          appAuthor
        </button>
        <hr />
        <p>{{ selectedComponent }}</p>
        <hr />

        <!--componenetin destoryed olmaması yani her seferinde tekrardan üretilmemesi için kullanılır.-->
        <keep-alive>
          <!-- dinamik olarak render etmek için compenent ve bind attr kullanılır.-->
          <component :is="selectedComponent">
            <h1 slot="heading">Güzek bir gün</h1>
            <p slot="content">Bu gün hava karlı ve oldukça soğuk</p>
            <p>boş slot</p>
          </component>
        </keep-alive>

        <!-- <app-memory>
          <h1 slot="heading">Güzek bir gün</h1>
            <p slot="content">Bu gün hava karlı ve oldukça soğuk</p>
            <p>boş slot</p>
        </app-memory> -->
      </div>
    </div>
  </div>
</template>

<script>
import Memory from "./Componets/Memory.vue";
import Author from "./Componets/Author.vue";
import NewMemory from "./Componets/NewMemory.vue";

export default {
  components: {
    appMemory: Memory,
    appAuthor: Author,
    appNewMomory: NewMemory,
  },
  data: function () {
    return {
      selectedComponent: "appMemory",
    };
  },
};
</script>

