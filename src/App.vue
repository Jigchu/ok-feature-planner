<script setup>
import { ref } from 'vue';
import Task from './Task.vue';
import TaskHeadline from './TaskHeadline.vue';
import './style.css'
const count = ref(0)

function increment() {
    count.value++
}
</script>

<template>
    <div class="top-level">
        <TaskHeadline></TaskHeadline>
        <h1>You did it!</h1>
        <p>
            Visit <a href="https://vuejs.org/" target="_blank" rel="noopener">vuejs.org</a> to read the
            documentation
        </p>
        <button @click="increment">
            {{ count }}
        </button>
        <Task></Task>
    </div>
</template>
