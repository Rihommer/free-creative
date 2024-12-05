<script setup>

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
                    ../assets/images/Пюре-1200-1x.avif 2x"
                    media="(min-width: 993px)"
                    type="image/avif" />
                <source
                    srcset="../assets/images/Пюре-1200-1x.webp 1x,
                    ../assets/images/Пюр1200-1x.webp 2x"
                    media="(min-width: 993px)"
                    type="image/webp" />
                <source
                    srcset="../assets/images/Пюре-576-1x.avif 1x,
                    ../assets/images/Пюре-576-1x.avif 2x"
                    media="(min-width: 361px)"
                    type="image/avif" />
                <source
                    srcset="../assets/images/Пюре-576-1x.webp 1x,
                    ../assets/images/Пюр576-1x.webp 2x"
                    media="(min-width: 361px)"
                    type="image/webp" />
                <source
                    srcset="../assets/images/Пюре-360-1x.avif 1x,
                    ../assets/images/Пюре-360-1x.avif 2x"
                    media="(min-width: 320px)"
                    type="image/avif" />
                <source
                    srcset="../assets/images/Пюре-360-1x.webp 1x,
                    ../assets/images/Пюре-360-1x.webp 2x"
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

@media(min-width: 361px) {
    .about-style {
        padding-block-start: 92px;
    }

    .about-style__text {
        max-inline-size: 380px;
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
}

@media(min-width: 993px) {
    .about-style {
        padding-block-start: 70px;
    }
}
</style>