<template>
  <div>
    <template v-if="!theme"> Loading...</template>
    <component :is="'Themes' + theme" v-else />
  </div>
</template>

<script>
const _theme = 'theme2'

export default {
  layout(context) {
    // return context.data.theme
    return _theme
  },
  data: () => ({
    theme: null,
  }),
  async fetch() {
    this.theme = await 'Theme2'
  },
  fetchOnServer: true,
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
