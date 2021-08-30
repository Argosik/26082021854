<template>

    <CommentItem
    v-for="todo of Comms"
    v-bind:todo="todo"
    />
</template>

<script>
import CommentItem from '@/components/CommentItem'
export default {
    props: ['Comms'],
    components: {
        CommentItem
    }
}
</script>