<script setup>
    import { ref } from 'vue';
    import List from './List.vue';

    const list = ref([
        {
            title: 'Название компании'
        },
        {
            title: 'Логотип – основной графический символ'
        },
        {
            title: 'Фирменные цвета всей коммуникации (онлайн и оффлайн)'
        },
        {
            title: 'Шрифт'
        },
        {
            title: 'Носители фирменного стиля',
            text: 'Этот набор варьируется в зависимости от нужд и потребностей компании: визитные карточки, фирменные бланки и прочая деловая документация, упаковка, сувенирная продукция, брендинг автотранспорта.'
        }
    ]);
</script>

<template>
    <section class="about-style container">
        <h2 class="about-style__title">
            Что такое фирменный стиль
        </h2>
        <div class="about-style__box">
            <picture class="about-style__img">
                <source
                    srcset="../assets/images/Пюре-1200-1x.avif 1x,
                    ../assets/images/Пюре-1200-2x.avif 2x"
                    media="(min-width: 993px)"
                    type="image/avif" />
                <source
                    srcset="../assets/images/Пюре-1200-1x.webp 1x,
                    ../assets/images/Пюре-1200-2x.webp 2x"
                    media="(min-width: 993px)"
                    type="image/webp" />
                <source
                    srcset="../assets/images/Пюре-576-1x.avif 1x,
                    ../assets/images/Пюре-576-2x.avif 2x"
                    media="(min-width: 361px)"
                    type="image/avif" />
                <source
                    srcset="../assets/images/Пюре-576-1x.webp 1x,
                    ../assets/images/Пюре-576-2x.webp 2x"
                    media="(min-width: 361px)"
                    type="image/webp" />
                <source
                    srcset="../assets/images/Пюре-360-1x.avif 1x,
                    ../assets/images/Пюре-360-2x.avif 2x"
                    media="(min-width: 320px)"
                    type="image/avif" />
                <source
                    srcset="../assets/images/Пюре-360-1x.webp 1x,
                    ../assets/images/Пюре-360-2x.webp 2x"
                    media="(min-width: 320px)"
                    type="image/webp" />
                <img src="../assets/images/Пюре-1200-2x.webp" alt="Банки с пюре" width="302" height="181" />
            </picture>
            <div class="about-style__text">
                <p class="about-style__text-item">
                    Это набор тех уникальных &laquo;признаков&raquo;, по&nbsp;которым клиент отличит вас от&nbsp;других компаний. Фирменный стиль отражает миссию бренда, ценности, является способом его идентификации, формирует определённое восприятие в&nbsp;коммуникации с&nbsp;потребителями.
                </p>
                <p class="about-style__text-item">
                    Видеале разработка корпоративного стиля должна происходить одновременно с&nbsp;созданием бизнеса и&nbsp;формированием его фундаментальных идей. Есть и&nbsp;второй вариант: бизнес существует определенное время и&nbsp;ему нужен перезапуск&nbsp;&mdash; это называется редизайн или ребрендинг: в&nbsp;мире жёсткой конкуренции важно быть &laquo;в&nbsp;тренде&raquo;, успевать за&nbsp;изменениями в&nbsp;поведениях покупателя и&nbsp;&laquo;говорить&raquo; с&nbsp;ним на&nbsp;одном языке.
                </p>
            </div>
        </div>
        <div class="about-style__list">
            <p class="about-style__list-title">
                Название и&nbsp;логотип&nbsp;&mdash; важные составляющие фирменного стиля, но&nbsp;на&nbsp;этом всё только начинается. Ниже основные элементы:
            </p>
            <List
                :list="list"
            />
        </div>
    </section>
</template>

<style scoped>
.about-style {
	padding-block-start: 56px;
}

.about-style__box {
	margin-block-start: 15px;
}

.about-style__text {
	margin-block-start: 30px;
}

.about-style__text-item:not(:first-child) {
	margin-block-start: 1lh;
}

.about-style__list {
	margin-block-start: 90px;
}

.about-style__list-title {
    font-family: "20kopeekBook";
    font-size: 3.5rem;
    line-height: 1;
}

.list {
	margin-block-start: 39px;
}

@media(min-width: 361px) {
    .about-style {
        padding-block-start: 92px;
    }

    .about-style__text {
        max-inline-size: 380px;
    }

    .list {
	    margin-block-start: 52px;
    }
}


@media(min-width: 577px) {
    .about-style {
        padding-block-start: 100px;
    }

    .about-style__box {
        max-inline-size: 450px;
    }

    .about-style__text {
        max-inline-size: 460px;
    }

    .about-style__list {
        margin-block-start: 120px;
    }

    .about-style__list-title {
        font-size: 4.5rem;
    }

    .list {
        margin-block-start: 43px;
    }
}

@media(min-width: 769px) {
    .about-style {
        padding-block-start: 80px;
    }

    .about-style__box {
        display: flex;
        gap: 30px;

        max-inline-size: initial;
    }

    .about-style__img {
        flex: 1;
    }

    .about-style__text {
        flex: 1;
        margin-block-start: initial;
    }

    .list {
        margin-block-start: 40px;
    }
}

@media(min-width: 993px) {
    .about-style {
        padding-block-start: 70px;
    }

    .about-style__list {
        margin-block-start: 140px;
    }

    .about-style__list-title {
        font-size: 5.5rem;
    }
}
</style>