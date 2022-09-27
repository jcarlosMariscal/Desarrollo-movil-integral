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
    <h2 v-if="edad >= 18 && edad > 0 && edad < 80">Mayor de edad</h2>
    <h2 v-else-if="edad < 18 && edad > 0 && edad < 80">Menor de edad</h2>
    <h2 v-else>Edad inválida</h2>

    <button @click="inc()">Incrementar</button>
    <button @click="dis()">Disminuir</button>
    <br /><br />
    <hr />

    <h2>v-for</h2>
    <ul>
      <li>{{ usuarios[0] }}</li>
      <li>{{ usuarios[1] }}</li>
      <li>{{ usuarios[2] }}</li>
    </ul>
    <br />
    <h3>Empleando v-for</h3>
    <ul>
      <li v-for="(usuario, index) in usuarios">{{ index }}: {{ usuario }}</li>
    </ul>
    <br />
    <ul>
      <li v-for="(usuario, index) in usuarios" :key="index">
        {{ index }}: {{ usuario }}
      </li>
    </ul>
    <br />
    <ul>
      <li v-for="(valor, clave) in obUsuarios" :key="clave">
        {{ clave }}: {{ valor }}
      </li>
    </ul>
    <br />
    <hr />

    <h2>Empleando v-on</h2>
    <div v-on:click="click" class="contenedor">
      <b>Clicks: {{ clicks }}</b>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    titulo: "Hola desde VUE.js 3",
    html: "<b>Soy una b, dentro de un h3</b>",
    edad: 16,
    usuarios: ["Melisa", "Fernando", "Raúl", "José"],
    obUsuarios: { nombre: "Ofelia Mari" },
    clicks: 0,
  }),
  methods: {
    inc() {
      this.edad++;
    },
    dis() {
      this.edad--;
    },
    click() {
      this.clicks++;
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
.contenedor {
  background-color: aqua;
  color: palevioletred;
  font-weight: bolder;
  height: 200px;
}
</style>
