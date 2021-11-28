<template lang="pug">
  img.logo(src="/logo.png")
</template>
<script>
export default {
  name: "Logo",
}
</script>

<style lang="scss">
.logo {
  height: 100px;
  max-height: 100%;
  max-width: 100%;
  margin: 0 auto;
  grid-column-start: 1;
  grid-column-end: 4;
}
</style>
