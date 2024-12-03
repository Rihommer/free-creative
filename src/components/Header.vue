<script setup>
    import { ref } from 'vue';
    import Social from './Social.vue';
    import facebookIcon from './icons/facebook.svg';
    import instagramIcon from './icons/instagram.svg';

    const socials = ref([
    {
        href: 'javascript: void(0)',
        src: facebookIcon,
        alt: 'Facebook'
    },
    {
        href: 'javascript: void(0)',
        src: instagramIcon,
        alt: 'Instagram'
    }
]);
</script>

<template>
    <header class="header">
        <a class="header__logo" href="javascript: void(0)">
            <img class="header__logo-img" src="./icons/logo.svg" alt="FREE" width="84" height="36">
        </a>
        <div class="header__text">Разрабатываем фирменные стили с 2009 года</div>
        <button class="burger"></button>
        <div class="header__box">
            <a class="header__telephone" href="tel:+74951563911">8 (495) 156-39-11</a>
            <Social
                v-for="social in socials"
                :href = social.href
                :src = social.src
                :alt = social.alt
                :key = social.alt
            />
        </div>

    </header>
</template>

<style scoped>
.header {
	display: flex;
	align-items: center;

	color: #fff;
}

.header__text {
	max-width: 14ch;
	margin-inline-start: 20px;

	font-size: 1.2rem;
	line-height: 1.1;
}

.burger {
	width: 30px;
	height: 18px;

	margin-inline-start: auto;

	background: repeating-linear-gradient(var(--font-color) 0 2px, #0000 2px 6px);
	border: 0;

	cursor: pointer;
}

.header__box {
    display: none;
}

.header__telephone {
	padding-inline: 33px;

	font-size: 1.6rem;
	line-height: 34px;
	color: inherit;
	text-decoration: none;

	border: 1px solid currentColor;
	border-radius: 15px;
}

@media (min-width: 576px) {
    .header__text {
        align-self: flex-end;
        max-width: 23ch;
        line-height: 1.3;
    }
}

@media (min-width: 768px) {
    .header__text {
        font-size: 1.4rem;
    }
}

@media (min-width: 992px) {
    .burger {
        display: none;
    }

    .header__box {
        display: flex;
        gap: 28px;

        margin-inline-start: auto;
    }
}

@media (min-width: 1200px) {
    .header__text {
        font-size: 1.5rem;
    }
}
</style>