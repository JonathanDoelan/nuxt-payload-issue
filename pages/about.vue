<template>
    <div>
        <p>{{ data }}</p>
    </div>
</template>



<script setup>
const { data } = await useAsyncData('about', () => ({
    subpage: {
        title: 'about me'
    }
}));

useHead({ title: data.value.subpage.title });
</script>
