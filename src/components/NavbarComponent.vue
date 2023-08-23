<template>
  <div>
    <nav
      class="navbar navbar-expand-lg bg-dark border-bottom border-body"
      data-bs-theme="dark"
    >
      <div class="container-fluid">
        <a class="navbar-brand" href="/">Cursos AlfaWeb</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
            <li class="nav-item mx-3" v-for="ruta in rutas" :key="ruta.name">
              <router-link
                :to="ruta.path"
                class="nav-link active"
                aria-current="page"
                >{{ ruta.name }}</router-link
              >
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavbarComponent",
  data() {
    return {
      rutas: [
        {
          path: "/",
          name: "Home",
        },
        {
          path: "/administracion",
          name: "Administracion",
        },
        
      ],
    };
  },
};
</script>

<style scoped>
</style>