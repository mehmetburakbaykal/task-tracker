<template>
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>{{ task.text }}
            <i @click="onDelete(task.id)" class="fa-regular fa-circle-xmark"></i>
        </h3>
        <h3>{{ task.day }}</h3>
    </div>

</template>

<script>
export default {
    name: "Task",
    props: {
        task: Object,
    },
    methods: {
        onDelete(id) {
            this.$emit("delete-task", id)
        }
    }
}
</script>

<style scope>
.fa-regular {
    color: red;
}

i {
    border: none;
    cursor: pointer;
}

.task {
    width: 40vh;
    background: #f4f4f4;
    border-radius: 2px;
    margin: 5px;
    padding: 10px 20px;
}

.task.reminder {
    border-left: 5px solid green;
}

.task h3 {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>