<script setup>
    import Header from './components/Header.vue';
    import Intro from './components/Intro.vue';
</script>

<template>
  <Header />
  <main>
    <Intro />
  </main>
</template>

<style scoped>
.header {
	margin-block-start: var(--header-margin-block-start);
}
</style>