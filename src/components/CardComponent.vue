<template>
  <div class="container">
    <div class="row">
      <div class="col-md-4" v-for="(curso,index) in cursos" :key="index">
        <div class="card mt-4" style="width: 18rem">
          <img :src="curso.img" class="card-img-top" :alt="curso.nombre" />
          <div class="card-body">
            <h5 class="card-title text-start">{{ curso.nombre }}</h5>
            <p class="card-text text-start">
              Información
            </p>
          </div>
          <ul class="list-group list-group-flush text-start">
            <li class="list-group-item">Costo:{{ curso.costo }} <p>Duración: {{ curso.duracion }}</p></li>
            <li class="list-group-item">Cupos:{{ curso.cupos }} <p>Completado: {{ curso.completado }}</p></li>
            <li class="list-group-item">Fecha de Registro: <p>{{ curso.fecha_registro }}</p> </li>
            <li class="list-group-item">Descripción: <p>{{ curso.descripcion }}</p></li>
          </ul>
          <div class="card-body">
            <a href="#" class="card-link">Card link</a>
            <a href="#" class="card-link">Another link</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "CardComponent",
  computed: {
    ...mapState(["cursos"]),
  },
};
</script>

<style scoped>
</style>