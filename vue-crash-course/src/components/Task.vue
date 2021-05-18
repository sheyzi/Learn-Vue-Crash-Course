<template>
    <div
        :class="[
            task.reminder ? 'border-green-600 border-l-4' : 'task',
        ]"
        class="bg-gray-200 p-2 mb-1"
        style="cursor: pointer"
    >
        <h3 class="text-lg font-semibold flex justify-between">
            {{ task.text }}
            <span @click="deleteTask(task.id)" class="text-red-600 px-4 "
                ><i class="fas fa-times" ></i
            ></span>
        </h3>
        <p class="text-sm">{{ task.day }}</p>
    </div>
</template>

<script>
export default {
    name: 'Task',
    props: {
        task: Object,
    },
    methods: {
        deleteTask(id) {
            this.$emit('delete-task', id)
        }
    }
};
</script>