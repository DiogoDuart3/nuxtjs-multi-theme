<template>
  <div>
    <ThemesTheme2Header />
    <Nuxt />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Tema 2',
      link: [
        {
          rel: 'stylesheet',
          href: require('~/assets/theme2/main.scss'),
        },
      ],
    }
  },
}
</script>
