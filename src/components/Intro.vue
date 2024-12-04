<script setup>
    import { ref } from 'vue';
    import Link from './Link.vue';

    const links = ref([
        {
            href: 'javascript: void(0)',
            text: 'Портфолио'
        },
        {
            href: 'javascript: void(0)',
            text: 'Оставить заявку'
        }
    ])
</script>

<template>
    <section class="intro">
        <div class="container">
            <H1 class="intro__title">
                Вам нужен фирменный стиль или ребрендинг?
            </H1>
            <p class="intro__text">
                Разработаем в срок от 10-ти дней
            </p>
            <div class="intro__box">
                <Link
                    v-for="link in links"
                    :href="link.href"
                    :text="link.text"
                />
            </div>
        </div>

    </section>
</template>

<style scoped>
    .intro {
        min-height: 640px;

        margin-block-start: calc(0px - var(--header-height-full));
        padding-block-start: var(--header-height-full);

        color: #fff;
        background-image:
            image-set(
                url(../assets/images/intro-360x1.avif) type("image/avif") 1x,
                url(../assets/images/intro-360x2.avif) type("image/avif") 2x,
                url(../assets/images/intro-360x1.webp) type("image/webp") 1x,
                url(../assets/images/intro-360x2.webp) type("image/webp") 2x
            ),
            linear-gradient(#0830a2 0 0)
    }

    .intro__title {
        margin-block-start: 82px;

        font-size: 3rem;
        line-height: 1.1;
    }

    .intro__text {
        max-width: 16ch;
        margin-block-start: 15px;

        font-size: 2rem;
        line-height: 1.1;
    }

    .intro__box {
        display: inline-flex;
        flex-direction: column-reverse;
        align-items: flex-start;
        gap: 20px;

        margin-block-start: 40px;
    }

    @media(min-width: 360px) {
        .intro {
            min-height: 496px;
            background-image:
                image-set(
                    url(../assets/images/intro-576x1.avif) type("image/avif") 1x,
                    url(../assets/images/intro-576x2.avif) type("image/avif") 2x,
                    url(../assets/images/intro-576x1.webp) type("image/webp") 1x,
                    url(../assets/images/intro-576x2.webp) type("image/webp") 2x
                ),
                linear-gradient(#0830a2 0 0)
        }

        .intro__title {
            margin-block-start: 86px;
        }

        .intro__box {
            flex-direction: row;
            flex-wrap: wrap;
            gap: 35px;

            margin-block-start: 25px;
        }
    }

    @media(min-width: 576px) {
        .intro {
            min-height: 1024px;
            background-image:
                image-set(
                    url(../assets/images/intro-768x1.avif) type("image/avif") 1x,
                    url(../assets/images/intro-768x2.avif) type("image/avif") 2x,
                    url(../assets/images/intro-768x1.webp) type("image/webp") 1x,
                    url(../assets/images/intro-768x2.webp) type("image/webp") 2x
                ),
                linear-gradient(#0830a2 0 0)
        }

        .intro__title {
            max-width: 18ch;
            margin-block-start: 244px;

            font-family: "20kopeekBook";
            font-size: 4.5rem;
            line-height: 1;
        }

        .intro__text {
            max-width: initial;
            margin-block-start: 25px;
            font-size: 2.6rem;
        }

        .intro__box {
            flex-direction: column;
            align-items: stretch;
            gap: 42px;

            margin-block-start: 78px;
        }
    }

    @media(min-width: 768px) {
        .intro {
            min-height: 768px;
            color: var(--font-color);
            background-image:
                image-set(
                    url(../assets/images/intro-992x1.avif) type("image/avif") 1x,
                    url(../assets/images/intro-992x2.avif) type("image/avif") 2x,
                    url(../assets/images/intro-992x1.webp) type("image/webp") 1x,
                    url(../assets/images/intro-992x2.webp) type("image/webp") 2x
                ),
                linear-gradient(#2f94dd 0 0)
        }

        .intro__title {
            margin-block-start: 228px;
        }

        .intro__box {
            flex-direction: row;
            align-items: stretch;
            gap: 30px;

            margin-block-start: 55px;
        }
    }

    @media(min-width: 992px) {
        .intro {
            min-height: 945px;
            background-image:
                image-set(
                    url(../assets/images/intro-1200x1.avif) type("image/avif") 1x,
                    url(../assets/images/intro-1200x2.avif) type("image/avif") 2x,
                    url(../assets/images/intro-1200x1.webp) type("image/webp") 1x,
                    url(../assets/images/intro-1200x2.webp) type("image/webp") 2x
                ),
                linear-gradient(#2f94dd 0 0)
        }

        .intro__title {
            margin-block-start: 277px;
            font-size: 5.5rem;
        }

        .intro__text {
            margin-block-start: 30px;
            font-size: 3.4rem;
        }

        .intro__box {
            gap: 20px;
            margin-block-start: 65px;
        }
    }
</style>