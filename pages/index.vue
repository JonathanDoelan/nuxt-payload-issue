<template>
    <div>
        <p>{{ data }}</p>
    </div>
</template>



<script setup>
const { data } = await useAsyncData('index', () => ({
    index: {
        page: 'home'
    }
}));

useHead({ title: data.value.index.page });
</script>
