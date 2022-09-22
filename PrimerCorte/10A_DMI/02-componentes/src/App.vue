<template>
  <h1>Componentes en VUE</h1>
  <hr />
  <card url="https://cdn.svgporn.com/logos/vue.svg" nombre="Vue.js" />
  <card url="https://cdn.svgporn.com/logos/angular-icon.svg" nombre="Angular" />
  <card url="https://cdn.svgporn.com/logos/vuetifyjs.svg" nombre="Vuetify" />
  <card url="https://cdn.svgporn.com/logos/react.svg" nombre="React" />
  <button
    type="button"
    class="btn btn-primary"
    data-toggle="modal"
    data-target="#modal"
  >
    Modal
  </button>
</template>
<script>
import Card from "./components/Card.vue";
import Slot from "./components/Slot.vue";
export default {
  components: { Card, Slot },
};
</script>
