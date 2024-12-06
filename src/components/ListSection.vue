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
    <section class="list-section container">
        <p class="list-section__title">
            Название и&nbsp;логотип&nbsp;&mdash; важные составляющие фирменного стиля, но&nbsp;на&nbsp;этом всё только начинается. Ниже основные элементы:
        </p>
        <List
            :list="list"
        />
    </section>
</template>

<style scoped>
.list-section {
	margin-block-start: 90px;
}

.list-section__title {
    font-family: "20kopeekBook";
    font-size: 3.5rem;
    line-height: 1;
}

.list {
	margin-block-start: 39px;
}

@media (min-width: 361px) {
    .list {
	    margin-block-start: 52px;
    }
}

@media (min-width: 577px) {
    .list-section {
        margin-block-start: 120px;
    }

    .list-section__title {
        font-size: 4.5rem;
    }

    .list {
        margin-block-start: 43px;
    }
}

@media (min-width: 769px) {
    .list {
        margin-block-start: 40px;
    }
}

@media (min-width: 993px) {
    .list-section {
        margin-block-start: 140px;
    }

    .list-section__title {
        font-size: 5.5rem;
    }
}
</style>