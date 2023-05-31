
<template>
    <div>
      <h1>{{ isUppercase ? title.toUpperCase() : title }}</h1>
    </div>
  </template>
  
  
  <script setup>
    const title ='My first component!';
    const isUppercase = false;
  </script>
  <style>
  h1 {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  </style>