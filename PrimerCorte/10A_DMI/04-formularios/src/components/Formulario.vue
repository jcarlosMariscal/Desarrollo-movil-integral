<template>
  <form @submit.prevent="addUser">
    <div class="form-group">
      <label for="exampleInputEmail1">Nombre</label>
      <input
        type="text"
        class="form-control"
        id="exampleInputEmail1"
        aria-describedby="emailHelp"
        placeholder="Enter Name"
        v-model="nombre"
      />
      <small id="emailHelp" class="form-text text-muted"
        >We'll never share your email with anyone else.</small
      >
    </div>
    <div class="form-group">
      <label for="exampleInputPassword1">Edad</label>
      <input
        type="number"
        class="form-control"
        id="exampleInputPassword1"
        placeholder="Age"
        v-model="edad"
      />
    </div>
    <div class="form-group">
      <label for="exampleInputPassword1">Correo</label>
      <input
        type="email"
        class="form-control"
        id="exampleInputPassword1"
        placeholder="Email"
        v-model="correo"
      />
    </div>
    <div class="form-check">
      <input type="checkbox" class="form-check-input" id="exampleCheck1" />
      <label class="form-check-label" for="exampleCheck1">Check me out</label>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
</template>

<script>
export default {
  data: () => ({
    nombre: "",
    edad: 0,
    correo: "",
  }),
  methods: {
    addUser() {
      console.log(this.nombre, this.edad, this.correo);
    },
  },
};
</script>
