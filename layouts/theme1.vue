<template>
  <div class="theme-theme1">
    <div>Header tema 1</div>
    <Nuxt />
    <div>Footer tema 1</div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Tema 1',
      link: [
        {
          rel: 'stylesheet',
          href: require('~/assets/theme1/main.scss'),
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped />
