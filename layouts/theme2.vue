<template>
  <div class="theme-theme2">
    <ThemesTheme2Header />
    <Nuxt />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Tema 2',
    }
  },
}
</script>

<style lang="scss" scoped>
.theme-theme2 {
  &::v-deep {
    @import '~/assets/theme2/main.scss';
  }
}
</style>
