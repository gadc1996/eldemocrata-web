<template lang="pug">
  header.header
    img.logo(src="/logo.png")
    nav.nav
      NuxtLink.nav__link(to="/") Home
      NuxtLink.nav__link(to="/") Home
</template>
<script>
export default {}
</script>

<style lang="scss">
.header {
  height: 100px;
  display: grid;
  grid-template-columns: 1fr 2fr;
  .logo {
    max-height: 100%;
    max-width: 100%;
  }
  .nav {
    background-color: gray;
  }
}
</style>
