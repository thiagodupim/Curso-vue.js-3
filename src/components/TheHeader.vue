<template>
    <header class="header">
        Header
    </header>
</template>

<script>
    export default {  
        mounted() {
            window.addEventListener('resize', this.resize);
        },

        // Destruir as nossas libs, Eventos e Listeners
        beforeUnmount() {
            console.log('beforeUnmount');
            window.removeEventListener('resize', this.resize);
        },

        unmounted() {
            console.log('unmounted');
        },
        
        methods: {
            resize($evt) {
                console.log($evt);
            },
        }
    }
</script>

<style>
    .header{
        background: #000;
        color: #fff;
    }
</style>