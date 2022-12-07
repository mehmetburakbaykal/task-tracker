<template>
    <button @click="onClick" :style="{ backgroundColor: color }" class="btn">{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String,
    },
    methods: {
        onClick() {
            alert("clicked");
        }
    }
}
</script>

<style scoped>
button {
    color: white;
    padding: 10px 18px;
    border: none;
    border-radius: 5px;
}
</style> 