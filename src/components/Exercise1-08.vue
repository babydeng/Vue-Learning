<script setup>
const triggerAlert = (index) => {
  alert(`Triggered ${index}`);
};
</script>

<template>
  <div>
    <h1>Triggering Vue Methods</h1>
    <ul>
      <li v-for="index in 5" :key="index">
        <button @click="triggerAlert(index)">Trigger {{ index }} </button>
      </li>
    </ul>
  </div>
</template>

<style>
button{
  margin: 10px;
}
</style>
