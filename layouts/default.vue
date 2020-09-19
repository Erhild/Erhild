<template>
  <div>
    <TheHeader />
    <div class="container">
      <Nuxt />
    </div>
  </div>
</template>

<style lang="postcss" scoped>
.container {
  @apply justify-center align-middle mx-auto;

  max-width: 42rem;
}
</style>
