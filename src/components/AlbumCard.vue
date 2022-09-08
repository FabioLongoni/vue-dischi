<template>
  <div class="card">
    <div class="card__content">
      <img :src="poster" alt="">
      <h3 class="album">{{ title }}</h3>
      <div class="info__album">
        <div class="author">{{ author }}</div>
        <div class="year">{{ year }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    poster: String,
    title: String,
    author: String,
    year: String,
  }
}
</script>

<style scoped lang="scss">
  @import '../style/card.scss';
</style>