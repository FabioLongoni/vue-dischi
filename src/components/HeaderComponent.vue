<template>
  <div class="header__logo">
    <a href="#">
      <img src="https://pnggrid.com/wp-content/uploads/2021/05/Spotify-PNG-Logo-768x767.png" alt="logo-spotify">
    </a>
    <div class="search__bar">
      <input v-model="search" @keyup.enter="$emit('search',search)" type="text">
      <select name="Genre" id="">
        <option value="Genre" default>Genre</option>
        <option value="Rock">Rock</option>
        <option value="Metal">Metal</option>
        <option value="Jazz">Jazz</option>
        <option value="Pop">Pop</option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search:'',
    }
  }
}
</script>

<style scoped lang="scss">
  @import '../style/variables';

  .header__logo {
    background-color: $bg__color__light;
    padding: 0.5rem 1.5rem;
    display: flex;
    gap: 2rem;
    align-items: center;
    img {
      width: 35px;
    }
  }
</style>