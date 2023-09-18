<script >
export default {
    props: {
        messages: {
            type: Array,
            default: ["Hi", "Hello", "Howdy", "Hey there"]
        }
    },
    data() {
        return { message: this.messages[0], }
    },
    methods: {
        randomMessage: function() {
            this.message = this.messages[(Math.floor(Math.random() * this.messages.length))];
        }
    }
}

// import { ref } from "vue";
// const props = defineProps({
//     messages: Array
// })

// const message = ref(props.messages[0]);

// function randomMessage() {
//     message.value = props.messages[(Math.floor(Math.random() * props.messages.length))];
// }
</script>
<template>
    <div class="vue-component">
        <h3>This is a Vue component :O </h3>
        <h3>{{ message }}! Thank for visiting my blog!</h3>
        <button v-on:click="randomMessage">New greeting</button>
    </div>
</template>
<style>
.vue-component {
    border: 2px solid rgb(35, 163, 31);
}
</style>