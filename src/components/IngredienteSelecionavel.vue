<script lang="ts">
    import Tag from './Tag.vue';
    export default {
        components: { Tag },
        props: {
            ingrediente: { type: String, required: true }
        }
    }
</script>
<template>
    <Tag :texto="ingrediente" />
</template>