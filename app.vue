<script setup>
const { data } = await useAsyncData('count', () => $fetch('/counter'));
</script>

<template>Page visits: {{ data }}</template>
