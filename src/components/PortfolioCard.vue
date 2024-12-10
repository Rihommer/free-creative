<script setup>
    import Link from './Link.vue';

    const props = defineProps({
        picture: Object,
        title: String,
        text: String,
        link: {
            text: String,
            href: String
        }
    });

    const imageSizes = [
        { media: '(min-width: 993px)', avif: 'minWidth993px', webp: 'minWidth993px' },
        { media: '(min-width: 769px)', avif: 'minWidth769px', webp: 'minWidth769px' },
        { media: '(min-width: 577px)', avif: 'minWidth577px', webp: 'minWidth577px' },
        { media: '(min-width: 361px)', avif: 'minWidth361px', webp: 'minWidth361px' },
        { media: '(min-width: 1px)',   avif: 'minWidth1px',   webp: 'minWidth1px' }
    ];
</script>

<template>
    <article class="portfolio-card">
        <picture class="portfolio-card__img">
            <template v-for="size in imageSizes" :key="size.media">
                <source
                    :srcset="`${picture.avif[size.avif]['1x']} 1x, ${picture.avif[size.avif]['2x']} 2x`"
                    :media="size.media"
                    type="image/avif"
                />
                <source
                    :srcset="`${picture.webp[size.webp]['1x']} 1x, ${picture.webp[size.webp]['2x']} 2x`"
                    :media="size.media"
                    type="image/webp"
                />
            </template>
        <img :src="picture.src" :alt="picture.alt" :width="picture.width" :height="picture.height" />
        </picture>
        <div class="portfolio-card__box">
            <div class="portfolio-card__box-text">
                <h3 class="portfolio-card__title">{{ title }}</h3>
                <p class="portfolio-card__text">{{ text }}</p>
            </div>
            <Link class="link--bordered"
                :text="link.text"
                :href="link.href"
            />
        </div>
    </article>
</template>

<style scoped>
.portfolio-card__box {
	margin-block-start: 15px;
}

.portfolio-card__title {
	font-family: "20kopeekBook";
	font-size: 3.5rem;
	line-height: 1;
}

.portfolio-card__text {
    max-inline-size: 21ch;
	margin-block-start: 11px;

	line-height: 1.4;
}

.link {
	margin-block-start: 30px;
}

@media (min-width: 361px) {
    .portfolio-card__title {
        line-height: 1.4;
    }

    .portfolio-card__text {
        margin-block-start: 17px;
    }
}

@media (min-width: 484px) {
    .portfolio-card__box {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;

        margin-block-start: 27px;
    }

    .link {
        margin-block-start: 0;
    }
}

@media (min-width: 577px) {
    .portfolio-card__box {
        justify-content: start;
        gap: 24px;

        margin-block-start: 25px;
    }

    .portfolio-card__title {
        font-size: 4.5rem;
    }

    .portfolio-card__text {
        margin-block-start: 0;
    }
}

@media (min-width: 769px) {
    .portfolio-card__box {
        margin-block-start: 40px;
        gap: 100px;
    }
}

@media (min-width: 993px) {
    .portfolio-card__box {
        gap: 89px;
    }

    .portfolio-card__title {
        font-size: 5.5rem;
        line-height: 1.3;
    }
}
</style>