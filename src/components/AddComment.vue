<template>
    <form @submit.prevent="onSubmit">
        <input type="text" v-model="title">
        <button type="submit"> Комментировать </button>
    </form>
</template>
<script>
export default {
    data() {
        return {
            title: ''
        }
    },
    methods: {
        onSubmit() {
        if (this.title.trim()) {
            const newTodo = {
                id: Date.now(),
                title: this.title,
                
            }
        this.$emit('add-todo', newTodo)
        }
        }
    }
}
</script>
<style scoped>
    form {
        display: flex;
    }
    input {
        background: darkblue;
        color: white;
        width: 200px;
        height: 50px;
    }
</style>