<template>
    <div>
        <h1 v-show="true" v-once v-text="text" />
        <h2 v-html="html" v-show="false"/>
        <a  :href= link.url
            :title= link.title
            :tabindex= link.tabindex
            :target= link.target>
            {{ link.title }} </a>
    </div>
</template>
<script setup>
    const text = 'Directive text';
    const html = 'Stylise</br>HTML in<br/><b>your data</b>';
    const link = {
        title: "Go to Google",
        url: "https://google.com",
        tabindex: 1,
        target: "_blank",
    };
</script>
