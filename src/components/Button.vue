<script setup>
    defineProps(['buttonText'])
</script>

<template>
    <button class="button">{{ buttonText }}</button>
</template>

<style scoped>
.button {
	padding: 14px 47px;

	font-family: "20kopeek";
	font-size: 1.5rem;
	line-height: 1.4;
	color: #fff;

	border: none;
	border-radius: 40px;
	background-color: var(--strong-color);
}

.button--tall {
    padding-block: 19px;

    font-family: "20kopeekBook";
    font-size: 2rem;
    line-height: 1.1;
}

@media (min-width: 577px) {
    .button {
        font-size: 1.6rem;
        padding-block: 19px;
    }

    .button--tall {
        padding-block: 23px;
    }
}

@media (min-width: 993px) {
    .button {
        font-size: 1.8rem;
        padding-block: 23px;
    }

    .button--tall {
        font-size: 2.6rem;
    }
}
</style>