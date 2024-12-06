<script setup>
    defineProps(['list']);
</script>

<template>
    <ol class="list">
        <li v-for="(item, index) in list" :key="index" class="list__item">
            <div class="list__box">
                <p class="list__title">{{ item.title }}</p>
                <p v-if="item.text" class="list__text">{{ item.text }}</p>
            </div>
        </li>
    </ol>
</template>

<style scoped>
.list {
    padding: 0;

	list-style: none;
    counter-reset: list;
}

.list__item {
	display: flex;
	align-items: baseline;
	gap: 51px;

    &::before {
        font-family: "20kopeekBook";
        font-size: 3.5rem;
        counter-increment: list;
        content: counter(list);
    }
}

.list__title {
	line-height: 1.4;
}

.list__text {
    margin-block-start: 20px;

	font-size: 1.2rem;
	line-height: 1.3;
}

@media (min-width: 361px) {
    .list__box {
        max-inline-size: 259px;
    }

    .list__item {
        gap: 67px;
    }

    .list__text {
        margin-block-start: 10px;
    }
}

@media (min-width: 577px) {
    .list {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 91px;
    }

    .list__item {
        gap: 8px;

        &:last-child {
	        grid-column: span 2;
        }

        &::before {
            font-size: 4.5rem;
        }
    }

    .list__title {
        line-height: 1.3;
    }

    .list__text {
        margin-block-start: 14px;
        font-size: 1.4rem;
    }
}

@media (min-width: 769px) {
    .list {
        grid-template-columns: repeat(6, 1fr);
        gap: 43px;
    }

    .list__text {
        margin-block-start: 16px;
    }
}

@media (min-width: 993px) {
    .list__item::before {
        font-size: 5.5rem;
    }

    .list__title {
        line-height: 1.4;
    }

    .list__text {
        font-size: 1.5rem;
    }
}
</style>