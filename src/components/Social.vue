<script setup>
    const social = defineProps(['href', 'src', 'alt']);
</script>

<template>
    <a class="social" :href=href>
        <img class="social__img" :src=src :alt=alt width="13" height="13">
    </a>
</template>

<style scoped>
.social {
	display: grid;
	place-content: center;

	width: 36px;
	aspect-ratio: 1;

	border: 1px solid #fff;
	border-radius: 50%;
}
</style>