<script setup>
const information = {
  title: "My list component information",
  subtitle: "Vue JS basic",
  items: ["Looping", "Data", "Methods"],
}
</script>

<template>
  <div>
    <div v-for="(value, key) in information" :key="key">
      {{ key }}: {{ value }}
    </div>
  </div>
  </template>
  