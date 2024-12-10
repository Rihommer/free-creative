<script setup>
import { ref } from 'vue';
    import Header from './components/Header.vue';
    import Intro from './components/Intro.vue';
    import AboutStyle from './components/AboutStyle.vue';
    import StyleCost from './components/StyleCost.vue';

</script>

<template>
  <Header />
  <main>
    <Intro />
    <About-style />
    <StyleCost />
  </main>
</template>

<style scoped>
.header {
	margin-block-start: var(--header-margin-block-start);
}
</style>