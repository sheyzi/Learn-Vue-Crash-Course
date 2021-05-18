<template>
    <div
        class="p-5 w-85 border-2 border-solid m-2 h-auto border-gray-900"
    >
        <div class="mt-3">
            <Header title="Sheyzi Task Tracker"></Header>
            <Tasks @delete-task="deleteTask" :tasks="tasks" />
        </div>
    </div>
</template>

<script>
import Header from './components/Header.vue';
import Tasks from './components/Tasks.vue';
export default {
    name: 'App',
    components: {
        Header,
        Tasks,
    },
    data() {
        return {
            tasks: [],
        };
    },
    methods: {
        deleteTask(id) {
            if (confirm('Are you sure??')) {
                this.tasks = this.tasks.filter(
                    (task) => task.id !== id,
                );
            }
        },
    },
    created() {
        this.tasks = [
            {
                id: 1,
                text: 'Call Mummy',
                day: 'May 17 at 7:54pm',
                reminder: true,
            },
            {
                id: 2,
                text: 'Call Daddy',
                day: 'May 19 at 8:04pm',
                reminder: true,
            },
            {
                id: 3,
                text: 'Wash Clothes',
                day: 'July 20 at 9:00am',
                reminder: false,
            },
        ];
    },
};
</script>
