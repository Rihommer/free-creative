<script setup>
    const link = defineProps(['text', 'href'])
</script>

<template>
    <a class="link" :href="href">{{ text }}</a>
</template>

<style scoped>
    .link {
        display: inline-block;
        padding: 13.5px 47px;

        font-size: 1.5rem;
        line-height: 21px;
        color: var(--font-color);
        text-decoration: none;

        border: 1px solid #fff;
        border-radius: 40px;
        background-color: #fff;
    }

    .link--border {
        border-color: #000;
    }

    @media(min-width: 577px) {
        .link {
            padding-block: 18px;

            font-size: 1.6rem;
            line-height: 1.4;
        }
    }
</style>