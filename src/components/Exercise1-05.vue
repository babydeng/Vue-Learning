<template>
    <div>
    <h1>Looping through arrays</h1>
    <ul>
        <li v-for="(item, index) in interests" :key="index">
            {{ item }}</li>
    </ul>
    </div>  
</template>


<script setup>
const interests = ['TV', 'Games','Sports']
</script>

