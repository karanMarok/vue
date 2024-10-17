<template>
    <button class="dark:text-white">Go Dark</button>
    <div class="flex justify-center dark:bg-black h-[100vh]">
        <div class="bg-gray-200 border-2 border-black w-6/12">
            <h1 class="m-2 p-2">To Do List</h1>
            <input type="text" placeholder="Enter task here..."
                class="border-black border-1 bg-white rounded-md w-6/12 m-4 p-2" v-model="taskToAdd" />

            <button type="button" class="bg-black text-white rounded-lg p-2" @click="addTask">Add Task</button>

            <div class="p-2">
                <div v-for="(task, index) in taskList" :key="index" class="flex p-2">
                    <p class="w-6/12 border-black border-2 mr-2">{{ task }}</p>
                    <button type="button" class="bg-red-600 text-white rounded-lg p-2" @click="removeTask(index)">Remove
                        Task</button>
                </div>
            </div>

        </div>
    </div>

</template>

<script>
export default {
    data() {
        return {
            taskToAdd: "",
            taskList: [],
            darkMode: false
        }
    },
    methods: {
        addTask() {
            if (this.taskToAdd.length > 0) {
                this.taskList.push(this.taskToAdd);
            }
        },

        removeTask(index) {
            this.taskList.splice(index);
        },

        setDark() {
            this.darkMode = !darkMode
        }
    }

}
</script>