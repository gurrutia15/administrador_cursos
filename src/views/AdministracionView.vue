<template>
    <div>
        <h1>Vista Administración</h1>
        <TableComponent />
    </div>
</template>

<script>
import TableComponent from '@/components/TableComponent.vue';
    export default {
        name: "AdministracionView",
        components: {
            TableComponent,
        }
    }
</script>

<style scoped>

</style>