<script setup lang="ts">
// both are typed on initial install
// run npm run generate and then typings conflict with something in dist folder on anything using $fetch (i.e. second one)
const { data: typed } = useFetch('/api/counter')
const { data: notTyped } = useAsyncData('count', () => $fetch('/api/counter'));
</script>

<template>
<p>
    Page visits (typed): {{ typed }}
</p>
<p>
    Page visits (notTyped): {{ notTyped }}
</p>
</template>
