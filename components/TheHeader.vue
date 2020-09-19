<template>
  <header class="header">
    <nuxt-link to="/"> <Logo /> </nuxt-link>
    <div class="nav-items">
      <nuxt-link to="post">Blog</nuxt-link>
      <nuxt-link to="">Projects</nuxt-link>
    </div>
  </header>
</template>
<style lang="postcss">
.header {
  @apply flex justify-between p-4;
}
.nav-items {
  @apply grid gap-4 grid-flow-col;
}
</style>
