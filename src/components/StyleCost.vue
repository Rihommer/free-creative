<script setup>
    import { ref } from 'vue';
    import PortfolioCard from './PortfolioCard.vue';
    import Button from './Button.vue';

    import amperiaMinWidth993px2xJpg from './../assets/images/amperia-1200-2x.jpg';
    import amperiaMinWidth993px1xAvif from './../assets/images/amperia-1200-1x.avif';
    import amperiaMinWidth993px2xAvif from './../assets/images/amperia-1200-2x.avif';
    import amperiaMinWidth993px1xWebp from './../assets/images/amperia-1200-1x.webp';
    import amperiaMinWidth993px2xWebp from './../assets/images/amperia-1200-2x.webp';
    import amperiaMinWidth769px1xAvif from './../assets/images/amperia-992-1x.avif';
    import amperiaMinWidth769px2xAvif from './../assets/images/amperia-992-2x.avif';
    import amperiaMinWidth769px1xWebp from './../assets/images/amperia-992-1x.webp';
    import amperiaMinWidth769px2xWebp from './../assets/images/amperia-992-2x.webp';
    import amperiaMinWidth577px1xAvif from './../assets/images/amperia-768-1x.avif';
    import amperiaMinWidth577px2xAvif from './../assets/images/amperia-768-2x.avif';
    import amperiaMinWidth577px1xWebp from './../assets/images/amperia-768-1x.webp';
    import amperiaMinWidth577px2xWebp from './../assets/images/amperia-768-2x.webp';
    import amperiaMinWidth361px1xAvif from './../assets/images/amperia-576-1x.avif';
    import amperiaMinWidth361px2xAvif from './../assets/images/amperia-576-2x.avif';
    import amperiaMinWidth361px1xWebp from './../assets/images/amperia-576-1x.webp';
    import amperiaMinWidth361px2xWebp from './../assets/images/amperia-576-2x.webp';
    import amperiaMinWidth1px1xAvif from './../assets/images/amperia-360-1x.avif';
    import amperiaMinWidth1px2xAvif from './../assets/images/amperia-360-2x.avif';
    import amperiaMinWidth1px1xWebp from './../assets/images/amperia-360-1x.webp';
    import amperiaMinWidth1px2xWebp from './../assets/images/amperia-360-2x.webp';

    import AQLifecareMinWidth993px2xJpg from './../assets/images/aq-lifecare-1200-2x.jpg';
    import AQLifecareMinWidth993px1xAvif from './../assets/images/aq-lifecare-1200-1x.avif';
    import AQLifecareMinWidth993px2xAvif from './../assets/images/aq-lifecare-1200-2x.avif';
    import AQLifecareMinWidth993px1xWebp from './../assets/images/aq-lifecare-1200-1x.webp';
    import AQLifecareMinWidth993px2xWebp from './../assets/images/aq-lifecare-1200-2x.webp';
    import AQLifecareMinWidth769px1xAvif from './../assets/images/aq-lifecare-992-1x.avif';
    import AQLifecareMinWidth769px2xAvif from './../assets/images/aq-lifecare-992-2x.avif';
    import AQLifecareMinWidth769px1xWebp from './../assets/images/aq-lifecare-992-1x.webp';
    import AQLifecareMinWidth769px2xWebp from './../assets/images/aq-lifecare-992-2x.webp';
    import AQLifecareMinWidth577px1xAvif from './../assets/images/aq-lifecare-768-1x.avif';
    import AQLifecareMinWidth577px2xAvif from './../assets/images/aq-lifecare-768-2x.avif';
    import AQLifecareMinWidth577px1xWebp from './../assets/images/aq-lifecare-768-1x.webp';
    import AQLifecareMinWidth577px2xWebp from './../assets/images/aq-lifecare-768-2x.webp';
    import AQLifecareMinWidth361px1xAvif from './../assets/images/aq-lifecare-576-1x.avif';
    import AQLifecareMinWidth361px2xAvif from './../assets/images/aq-lifecare-576-2x.avif';
    import AQLifecareMinWidth361px1xWebp from './../assets/images/aq-lifecare-576-1x.webp';
    import AQLifecareMinWidth361px2xWebp from './../assets/images/aq-lifecare-576-2x.webp';
    import AQLifecareMinWidth1px1xAvif from './../assets/images/aq-lifecare-360-1x.avif';
    import AQLifecareMinWidth1px2xAvif from './../assets/images/aq-lifecare-360-2x.avif';
    import AQLifecareMinWidth1px1xWebp from './../assets/images/aq-lifecare-360-1x.webp';
    import AQLifecareMinWidth1px2xWebp from './../assets/images/aq-lifecare-360-2x.webp';

    import vilataMinWidth993px2xJpg from './../assets/images/vilata-1200-2x.jpg';
    import vilataMinWidth993px1xAvif from './../assets/images/vilata-1200-1x.avif';
    import vilataMinWidth993px2xAvif from './../assets/images/vilata-1200-2x.avif';
    import vilataMinWidth993px1xWebp from './../assets/images/vilata-1200-1x.webp';
    import vilataMinWidth993px2xWebp from './../assets/images/vilata-1200-2x.webp';
    import vilataMinWidth769px1xAvif from './../assets/images/vilata-992-1x.avif';
    import vilataMinWidth769px2xAvif from './../assets/images/vilata-992-2x.avif';
    import vilataMinWidth769px1xWebp from './../assets/images/vilata-992-1x.webp';
    import vilataMinWidth769px2xWebp from './../assets/images/vilata-992-2x.webp';
    import vilataMinWidth577px1xAvif from './../assets/images/vilata-768-1x.avif';
    import vilataMinWidth577px2xAvif from './../assets/images/vilata-768-2x.avif';
    import vilataMinWidth577px1xWebp from './../assets/images/vilata-768-1x.webp';
    import vilataMinWidth577px2xWebp from './../assets/images/vilata-768-2x.webp';
    import vilataMinWidth361px1xAvif from './../assets/images/vilata-576-1x.avif';
    import vilataMinWidth361px2xAvif from './../assets/images/vilata-576-2x.avif';
    import vilataMinWidth361px1xWebp from './../assets/images/vilata-576-1x.webp';
    import vilataMinWidth361px2xWebp from './../assets/images/vilata-576-2x.webp';
    import vilataMinWidth1px1xAvif from './../assets/images/vilata-360-1x.avif';
    import vilataMinWidth1px2xAvif from './../assets/images/vilata-360-2x.avif';
    import vilataMinWidth1px1xWebp from './../assets/images/vilata-360-1x.webp';
    import vilataMinWidth1px2xWebp from './../assets/images/vilata-360-2x.webp';

    import coralBlackMinWidth993px2xJpg from './../assets/images/coral-black-1200-2x.jpg';
    import coralBlackMinWidth993px1xAvif from './../assets/images/coral-black-1200-1x.avif';
    import coralBlackMinWidth993px2xAvif from './../assets/images/coral-black-1200-2x.avif';
    import coralBlackMinWidth993px1xWebp from './../assets/images/coral-black-1200-1x.webp';
    import coralBlackMinWidth993px2xWebp from './../assets/images/coral-black-1200-2x.webp';
    import coralBlackMinWidth769px1xAvif from './../assets/images/coral-black-992-1x.avif';
    import coralBlackMinWidth769px2xAvif from './../assets/images/coral-black-992-2x.avif';
    import coralBlackMinWidth769px1xWebp from './../assets/images/coral-black-992-1x.webp';
    import coralBlackMinWidth769px2xWebp from './../assets/images/coral-black-992-2x.webp';
    import coralBlackMinWidth577px1xAvif from './../assets/images/coral-black-768-1x.avif';
    import coralBlackMinWidth577px2xAvif from './../assets/images/coral-black-768-2x.avif';
    import coralBlackMinWidth577px1xWebp from './../assets/images/coral-black-768-1x.webp';
    import coralBlackMinWidth577px2xWebp from './../assets/images/coral-black-768-2x.webp';
    import coralBlackMinWidth361px1xAvif from './../assets/images/coral-black-576-1x.avif';
    import coralBlackMinWidth361px2xAvif from './../assets/images/coral-black-576-2x.avif';
    import coralBlackMinWidth361px1xWebp from './../assets/images/coral-black-576-1x.webp';
    import coralBlackMinWidth361px2xWebp from './../assets/images/coral-black-576-2x.webp';
    import coralBlackMinWidth1px1xAvif from './../assets/images/coral-black-360-1x.avif';
    import coralBlackMinWidth1px2xAvif from './../assets/images/coral-black-360-2x.avif';
    import coralBlackMinWidth1px1xWebp from './../assets/images/coral-black-360-1x.webp';
    import coralBlackMinWidth1px2xWebp from './../assets/images/coral-black-360-2x.webp';

    const cards = ref([
      {
        picture: {
          avif: {
              minWidth993px: {
                  '1x': amperiaMinWidth993px1xAvif,
                  '2x': amperiaMinWidth993px2xAvif
              },
              minWidth769px: {
                  '1x': amperiaMinWidth769px1xAvif,
                  '2x': amperiaMinWidth769px2xAvif
              },
              minWidth577px: {
                  '1x': amperiaMinWidth577px1xAvif,
                  '2x': amperiaMinWidth577px2xAvif
              },
              minWidth361px: {
                  '1x': amperiaMinWidth361px1xAvif,
                  '2x': amperiaMinWidth361px2xAvif
              },
              minWidth1px: {
                  '1x': amperiaMinWidth1px1xAvif,
                  '2x': amperiaMinWidth1px2xAvif
              }
          },
          webp: {
              minWidth993px: {
                  '1x': amperiaMinWidth993px1xWebp,
                  '2x': amperiaMinWidth993px2xWebp
              },
              minWidth769px: {
                  '1x': amperiaMinWidth769px1xWebp,
                  '2x': amperiaMinWidth769px2xWebp
              },
              minWidth577px: {
                  '1x': amperiaMinWidth577px1xWebp,
                  '2x': amperiaMinWidth577px2xWebp
              },
              minWidth361px: {
                  '1x': amperiaMinWidth361px1xWebp,
                  '2x': amperiaMinWidth361px2xWebp
              },
              minWidth1px: {
                  '1x': amperiaMinWidth1px1xWebp,
                  '2x': amperiaMinWidth1px2xWebp
              }
          },
          src: amperiaMinWidth993px2xJpg,
          alt: 'rerew',
          width: '290',
          height: '163'
        },
          title: 'Amperia',
          text: 'Бренд красивых сувениров и подарков для дома',
          link: {
              text: 'Смотреть проект',
              href: 'javascript: void(0)'
          }
      },
      {
        picture: {
          avif: {
              minWidth993px: {
                  '1x': AQLifecareMinWidth993px1xAvif,
                  '2x': AQLifecareMinWidth993px2xAvif
              },
              minWidth769px: {
                  '1x': AQLifecareMinWidth769px1xAvif,
                  '2x': AQLifecareMinWidth769px2xAvif
              },
              minWidth577px: {
                  '1x': AQLifecareMinWidth577px1xAvif,
                  '2x': AQLifecareMinWidth577px2xAvif
              },
              minWidth361px: {
                  '1x': AQLifecareMinWidth361px1xAvif,
                  '2x': AQLifecareMinWidth361px2xAvif
              },
              minWidth1px: {
                  '1x': AQLifecareMinWidth1px1xAvif,
                  '2x': AQLifecareMinWidth1px2xAvif
              }
          },
          webp: {
              minWidth993px: {
                  '1x': AQLifecareMinWidth993px1xWebp,
                  '2x': AQLifecareMinWidth993px2xWebp
              },
              minWidth769px: {
                  '1x': AQLifecareMinWidth769px1xWebp,
                  '2x': AQLifecareMinWidth769px2xWebp
              },
              minWidth577px: {
                  '1x': AQLifecareMinWidth577px1xWebp,
                  '2x': AQLifecareMinWidth577px2xWebp
              },
              minWidth361px: {
                  '1x': AQLifecareMinWidth361px1xWebp,
                  '2x': AQLifecareMinWidth361px2xWebp
              },
              minWidth1px: {
                  '1x': AQLifecareMinWidth1px1xWebp,
                  '2x': AQLifecareMinWidth1px2xWebp
              }
          },
          src: AQLifecareMinWidth993px2xJpg,
          alt: 'rerew',
          width: '290',
          height: '163'
        },
          title: 'AQ.Lifecare',
          text: 'Инновационная клиника внутривенной медицины',
          link: {
              text: 'Смотреть проект',
              href: 'javascript: void(0)'
          }
      },
      {
        picture: {
          avif: {
              minWidth993px: {
                  '1x': vilataMinWidth993px1xAvif,
                  '2x': vilataMinWidth993px2xAvif
              },
              minWidth769px: {
                  '1x': vilataMinWidth769px1xAvif,
                  '2x': vilataMinWidth769px2xAvif
              },
              minWidth577px: {
                  '1x': vilataMinWidth577px1xAvif,
                  '2x': vilataMinWidth577px2xAvif
              },
              minWidth361px: {
                  '1x': vilataMinWidth361px1xAvif,
                  '2x': vilataMinWidth361px2xAvif
              },
              minWidth1px: {
                  '1x': vilataMinWidth1px1xAvif,
                  '2x': vilataMinWidth1px2xAvif
              }
          },
          webp: {
              minWidth993px: {
                  '1x': vilataMinWidth993px1xWebp,
                  '2x': vilataMinWidth993px2xWebp
              },
              minWidth769px: {
                  '1x': vilataMinWidth769px1xWebp,
                  '2x': vilataMinWidth769px2xWebp
              },
              minWidth577px: {
                  '1x': vilataMinWidth577px1xWebp,
                  '2x': vilataMinWidth577px2xWebp
              },
              minWidth361px: {
                  '1x': vilataMinWidth361px1xWebp,
                  '2x': vilataMinWidth361px2xWebp
              },
              minWidth1px: {
                  '1x': vilataMinWidth1px1xWebp,
                  '2x': vilataMinWidth1px2xWebp
              }
          },
          src: vilataMinWidth993px2xJpg,
          alt: 'rerew',
          width: '290',
          height: '163'
        },
          title: 'Vilata',
          text: 'Бренд натуральных и вкусных соусов',
          link: {
              text: 'Смотреть проект',
              href: 'javascript: void(0)'
          }
      },
      {
        picture: {
          avif: {
              minWidth993px: {
                  '1x': coralBlackMinWidth993px1xAvif,
                  '2x': coralBlackMinWidth993px2xAvif
              },
              minWidth769px: {
                  '1x': coralBlackMinWidth769px1xAvif,
                  '2x': coralBlackMinWidth769px2xAvif
              },
              minWidth577px: {
                  '1x': coralBlackMinWidth577px1xAvif,
                  '2x': coralBlackMinWidth577px2xAvif
              },
              minWidth361px: {
                  '1x': coralBlackMinWidth361px1xAvif,
                  '2x': coralBlackMinWidth361px2xAvif
              },
              minWidth1px: {
                  '1x': coralBlackMinWidth1px1xAvif,
                  '2x': coralBlackMinWidth1px2xAvif
              }
          },
          webp: {
              minWidth993px: {
                  '1x': coralBlackMinWidth993px1xWebp,
                  '2x': coralBlackMinWidth993px2xWebp
              },
              minWidth769px: {
                  '1x': coralBlackMinWidth769px1xWebp,
                  '2x': coralBlackMinWidth769px2xWebp
              },
              minWidth577px: {
                  '1x': coralBlackMinWidth577px1xWebp,
                  '2x': coralBlackMinWidth577px2xWebp
              },
              minWidth361px: {
                  '1x': coralBlackMinWidth361px1xWebp,
                  '2x': coralBlackMinWidth361px2xWebp
              },
              minWidth1px: {
                  '1x': coralBlackMinWidth1px1xWebp,
                  '2x': coralBlackMinWidth1px2xWebp
              }
          },
          src: coralBlackMinWidth993px2xJpg,
          alt: 'rerew',
          width: '290',
          height: '163'
        },
          title: 'Coral Black',
          text: 'Черная икра в современной инторпритации',
          link: {
              text: 'Смотреть проект',
              href: 'javascript: void(0)'
          }
      }
    ])
</script>

<template>
    <section class="style-cost container">
        <div class="style-cost__box">
            <div class="style-cost__box-title">
                <h2 class="style-cost__title">
                    Сколько стоит фирменный стиль?
                </h2>
                <picture class="style-cost__img">
                    <source
                        srcset="../assets/images/aq-lifecare-768-1x-2.avif 1x,
                        ../assets/images/aq-lifecare-768-2x-2.avif 2x"
                        media="(min-width: 576px)"
                        type="image/avif" />
                    <source
                        srcset="../assets/images/aq-lifecare-768-1x-2.webp 1x,
                        ../assets/images/aq-lifecare-768-2x-2.webp 2x"
                        media="(min-width: 576px)"
                        type="image/webp" />
                    <source
                        srcset="../assets/images/aq-lifecare-576-1x-2.avif 1x,
                        ../assets/images/aq-lifecare-576-2x-2.avif 2x"
                        media="(min-width: 361px)"
                        type="image/avif" />
                    <source
                        srcset="../assets/images/aq-lifecare-576-1x-2.webp 1x,
                        ../assets/images/aq-lifecare-576-2x-2.webp 2x"
                        media="(min-width: 361px)"
                        type="image/webp" />
                    <source
                        srcset="../assets/images/aq-lifecare-360-1x-2.avif 1x,
                        ../assets/images/aq-lifecare-360-2x-2.avif 2x"
                        media="(min-width: 1px)"
                        type="image/avif" />
                    <source
                        srcset="../assets/images/aq-lifecare-360-1x-2.webp 1x,
                        ../assets/images/aq-lifecare-360-2x-2.webp 2x"
                        media="(min-width: 1px)"
                        type="image/webp" />
                    <img src="../assets/images/aq-lifecare-768-2x-2.jpg" alt="aq.lifecare" width="289" height="175" />
                </picture>
            </div>
            <div class="style-cost__text">
                <p class="style-cost__text-item">
                    Каждая задача по разработке фирменного стиля уникальна для нас — это новый вызов и новые эмоции. Мы принципиально не предлагаем вам стандартизированные пакеты “эконом”, “стандрат”, или “премиум”, мы не штампуем, мы - создаем.
                </p>
                <p class="style-cost__text-item">
                    Стоимость разработки фирменного стиля в нашем агентстве начинается от 120 000 руб., финальную планку без брифинга определить невозможно - давайте созвонимся и обсудим ваш проект!
                </p>
                <p class="style-cost__text-item p--colored">
                    Каждый клиент нашего агентства получает приятный бонус на финише проекта, о котором мы расскажем ниже ▼
                </p>
            </div>
        </div>
        <div id="portfolio" class="style-cost__portfolio">
            <PortfolioCard v-for="card in cards"
                :title="card.title"
                :text="card.text"
                :link="card.link"
                :picture="card.picture"
            />
            <Button
                class="button--tall"
                button-text="Отправить заявку"
            />
        </div>
    </section>
</template>

<style scoped>
.style-cost {
	margin-block-start: 140px;
}

.style-cost__img {
	margin-block-start: 15px;
}

.style-cost__text {
	margin-block-start: 30px;
}

.style-cost__text-item:not(:first-child) {
	margin-block-start: 1lh;
}

.style-cost__portfolio {
    margin-block-start: 101px;
}

.portfolio-card:not(:first-child) {
    margin-block-start: 60px;
}

.button {
	display: block;

	margin-block-start: 90px;
	margin-inline: auto;
}

@media (min-width: 361px) {
    .style-cost {
        margin-block-start: 71px;
    }

    .style-cost__text {
        max-inline-size: 379px;
        margin-block-start: 20px;
    }

    .style-cost__portfolio {
        margin-block-start: 95px;
    }

    .portfolio-card:not(:first-child) {
        margin-block-start: 50px;
    }

    .button {
        margin-block-start: 50px;
    }
}

@media (min-width: 577px) {
    .style-cost {
        margin-block-start: 120px;
    }

    .style-cost__text {
        max-inline-size: 539px;
        margin-block-start: 25px;
    }

    .style-cost__portfolio {
        margin-block-start: 133px;
    }

    .button {
        margin-block-start: 20px;
    }
}

@media (min-width: 769px) {
    .style-cost__box {
        display: flex;
        flex-direction: row-reverse;
        gap: 30px;
        font-size: 3.4rem;
    }

    .style-cost__box-title {
        min-inline-size: 26ch;
    }

    .style-cost__text {
        max-inline-size: initial;
        margin-block-start: 1lh;
    }

    .style-cost__portfolio {
        margin-block-start: 120px;
    }
}

@media (min-width: 993px) {
    .style-cost__box {
        gap: 82px;
        font-size: 3.8rem;
    }

    .style-cost__portfolio {
        margin-block-start: 150px;
    }

    .portfolio-card:not(:first-child) {
        margin-block-start: 100px;
    }

    .button {
        margin-block-start: 50px;
    }
}
</style>