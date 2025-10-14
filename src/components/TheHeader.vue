<template>
    <header class="header">
        <h1 class="title">
            <slot name="title" />
        </h1>
        
        <div class="description">
            <slot name="description" /> 
        </div>
        
        <div>
            <slot />
        </div>
    </header>
</template>

<script>
    export default {  
        mounted() {
            console.log(this.$slots)
        }
    }
</script>

<style>
    .header{
        background: #000;
        color: #fff;
    }
</style>