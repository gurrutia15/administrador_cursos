<template>
  <div>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">Curso</th>
          <th scope="col">Cupos</th>
          <th scope="col">Inscritos</th>
          <th scope="col">Duración</th>
          <th scope="col">Costo</th>
          <th scope="col">Terminado</th>
          <th scope="col">Fecha</th>
          <th scope="col">Acciones</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(curso,index) in cursos" :key="index">
          <th scope="row">{{ curso.nombre }}</th>
          <td>{{ curso.cupos }} </td>
          <td>{{ curso.inscritos }}</td>
          <td>{{ curso.duracion }}</td>
          <td>{{ curso.costo }}</td>
          <td>{{ curso.completado }}</td>
          <td>{{ curso.fecha_registro }}</td>
          <td><span><svg width="2rem" height="auto" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
    <path fill="#eab308" d="M8.707 19.707L18 10.414L13.586 6l-9.293 9.293a1.003 1.003 0 0 0-.263.464L3 21l5.242-1.03c.176-.044.337-.135.465-.263zM21 7.414a2 2 0 0 0 0-2.828L19.414 3a2 2 0 0 0-2.828 0L15 4.586L19.414 9L21 7.414z"/>
</svg></span> <span><svg width="2rem" height="auto" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
    <path fill="#ef4444" d="M6 7H5v13a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2V7H6zm10.618-3L15 2H9L7.382 4H3v2h18V4z"/>
</svg></span></td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  name: "TableComponent",
  computed: {
    ...mapState(["cursos"])
  }
};
</script>

<style scoped>
</style>