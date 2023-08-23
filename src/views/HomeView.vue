<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <CardComponent />
  </div>
</template>

<script>
import CardComponent from "@/components/CardComponent.vue";
export default {
  name: 'HomeView',
  components: {
    CardComponent,
  }
}
</script>
