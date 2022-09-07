<template>
  <div class="header__logo">
    <a href="#">
      <img src="https://pnggrid.com/wp-content/uploads/2021/05/Spotify-PNG-Logo-768x767.png" alt="logo-spotify">
    </a>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
  @import '../style/variables';

  .header__logo {
    background-color: $bg__color__light;
    padding: 0.5rem 1.5rem;
    img {
      width: 40px;
    }
  }
</style>