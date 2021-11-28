<template lang="pug">
nav.nav(:class="[{ 'nav--visible': isNavBarVisible }]")
  NuxtLink.nav__link(to="/") Home
  NuxtLink.nav__link(to="/") Home
  NuxtLink.nav__link(to="/") Home
  NuxtLink.nav__link(to="/") Home
</template>
<script>
export default {
  name: "NavBar",
  props: {
    isNavBarVisible: {
      type: Boolean,
      default: false,
    }
  }
}
</script>

<style lang="scss">
.nav {
  display: none;
  .nav__link{
    width: auto;
    color: black;
    margin: 2rem ;
    font-size: 2rem;
    font-weight: 900;
    text-decoration: none;
    &:hover {
      color: white;
    }
  }
  
  &--visible{
    display: flex;
    flex-direction: column;
    background-color: gray;
    grid-column-start: 1;
    grid-column-end: 13;
  }
}
</style>
