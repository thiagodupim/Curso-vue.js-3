<template>
    <!-- <div :class="`alert alert-${variant}`"> -- Essa forma também funciona -->
    <div :class="baseClass">
        <slot />
        <button @click="onClick()">
            X
        </button>
    </div>
</template>

<script>
    export default {
        props: {
            variant: {
                type: String,
                default: ''
            },
        },

        computed: {
            baseClass() {
                return [
                    'alert',
                    this.variant ? `alert-${this.variant}` : ''
                ]
            },
        },

        methods: {
            onClick() {
                this.$emit('close') // Envia o evento pro pai
                console.log('clicou')
            }
        }
    }
</script>

<style scoped>
    .alert {
        display: flex;
        justify-content: space-between;
        padding: 5px;
        border-radius: 6px;
        color: gray;
        background: #ddd;
    }

    .alert-success {
        background: #42b983;
        color: #fff;
    }

    .alert-danger {
        background: red;
        color: #fff;
    }
</style>