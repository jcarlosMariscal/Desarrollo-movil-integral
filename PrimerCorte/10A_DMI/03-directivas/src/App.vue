<template>
  <div>
    <h1>Directivas en VUE.js</h1>
    <hr />
    <h2>v-text</h2>
    <span v-text="'Hola desde VUE.js'"></span>
    <br />
    <span>Hola desde VUE.js</span>
    <br />
    <span v-text="titulo"></span>
    <br />
    <span>Con IT: {{ titulo }}</span>
    <hr />

    <h2>v-html</h2>
    <h3 v-html="html"></h3>
    <hr />

    <h2>v-show</h2>
    <h3>Tu edad es: {{ edad }}</h3>
    <h2 v-show="edad >= 18">Eres mayor de edad</h2>
    <h2 v-show="edad < 18">Eres menor de edad</h2>

    <button @click="agre()">Agregar edad</button>
    <button @click="quit()">Quitar edad</button>
    <br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
  </div>
</template>
<script>
export default {
  data: () => ({
    titulo: "Hola desde VUE.js 3",
    html: "<b>Soy una b, dentro de un h3</b>",
    edad: 16,
  }),
  methods: {
    agre() {
      this.edad++;
    },
    quit() {
      this.edad--;
      s;
    },
  },
};
</script>
<style scoped>
div {
  text-align: center;
  margin: 0px 2rem;
}
h2 {
  color: tomato;
  font-size: 2rem;
}
</style>
