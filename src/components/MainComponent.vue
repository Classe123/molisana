<template>
    <main>
    <div class="container py-4">
      <h2 >>>> Content goes here <<<</h2>
    </div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent',
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    main{
        background-image: url('../assets/img/fondo-pag-speciali.jpg');
        h2{
            color: $bluetext;
            text-align: center;
        }
    }
</style>