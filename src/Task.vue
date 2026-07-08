<script setup>
import { useDraggable } from '@vueuse/core';
import { useTemplateRef } from 'vue';

const task = useTemplateRef("task")
const { x, y, style } = useDraggable(task, {
    preventDefault: true
})
</script>

<template>
    <div ref="task" :style="style" , style="position: fixed;">
        <h3>Im a task</h3>
        <p>Im cool and draggable :)</p>
    </div>
</template>
