<template>
    <header class="flex justify-between align-middle">
        <h1 class="font-semibold text-2xl">{{title}}</h1>
        <Button text="Add Task" color_class="bg-green-500"/>
    </header>
</template>

<script>
import Button from './Button.vue'
export default {
    name: 'Header',
    props: {
        title: String
    },
    components: {
        Button
    }
}
</script>

<style scoped>
    
</style>