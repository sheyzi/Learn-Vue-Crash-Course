<template>
    <button @click="addTask()" :class="color_class" class="py-1 px-2 text-white rounded">{{text}}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color_class: String,
    },
    methods: {
        addTask() {
            console.log('clicked')
        }
    }
}
</script>