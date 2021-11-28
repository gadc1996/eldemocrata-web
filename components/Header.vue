<template lang="pug">
  header.header
    Logo
    img.menu-toggle(@click='toggleNavBar' src="/menu-outline.svg")
    NavBar(:isNavBarVisible="isNavBarVisible")
</template>

<script>

export default {
  name: "Header",
  data: () => ({ 
    isNavBarVisible: false
  }),
  components: {
    NavBar: () => import('~/components/NavBar'),
    Logo: () => import('~/components/Logo'),
  },
  methods: {
    toggleNavBar() {
      this.isNavBarVisible = !this.isNavBarVisible
    }
  }
}
</script>

<style lang="scss">
.header {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
}
.menu-toggle {
  height: 50px;
  width: 50px;
  grid-column-start: 12;
  grid-column-end: 13;
  margin: auto;
}
</style>
