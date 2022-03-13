<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <br />
        <br />
        <button
          @click="selectedComponent = 'appBlue'"
          class="btn-sm btn btn-primary"
        >
          Mavi Temayı Yükle
        </button>
        <button
          @click="selectedComponent = 'appGreen'"
          class="btn-sm btn btn-warning"
        >
          Yeşil Temayı Yükle
        </button>
        <button
          @click="selectedComponent = 'appRed'"
          class="btn-sm btn btn-danger"
        >
          Kırmızı Temayı yükle
        </button>
        <hr />
        <p>{{ selectedComponent }}</p>
        <hr />

        <!--componenetin destoryed olmaması yani her seferinde tekrardan üretilmemesi için kullanılır.-->
        <keep-alive>
          <!-- dinamik olarak render etmek için compenent ve bind attr kullanılır.-->
          <component :is="selectedComponent">
            <h1 slot="blueComp">BU MAVİ COMPONENT</h1>
            <h1 slot="redComp">BU KIRMIZI COMPONENT</h1>
            <h1 slot="greenComp">BU YEŞİL COMPONENT</h1>
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
import Green from "./Componets/green.vue";
import Red from "./Componets/red.vue";
import Blue from "./Componets/blue.vue";

export default {
  components: {
    appBlue: Blue,
    appRed: Red,
    appGreen: Green,
  },
  data: function () {
    return {
      selectedComponent: "appBlue",
    };
  },
};
</script>
<style scoped>
h1{
  color: white;
}
</style>
