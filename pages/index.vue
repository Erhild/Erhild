<template>
  <div class="profile">
    <div class="avatar">
      <img src="erick.png" alt="me" />
    </div>
    <div class="introduction">
      <h3 class="greet text-center">Halo, Saya <b>Erick</b> 👋</h3>
      <p>
        saya seorang software engineer yang berdomisili di Tuban, Jawa Timur
      </p>
    </div>
  </div>
</template>

<style lang="postcss" scoped>
.profile {
  @apply p-16;
}
.avatar {
  overflow: hidden;
  border-radius: 4em;
  height: 8em;
  width: 8em;
  margin: -1em auto 2em;
  pointer-events: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.greet {
  font-weight: 300;
  font-size: 2rem;
  margin-bottom: 0.3rem;
}
b {
  font-weight: 700;
  font-family: Montserrat, sans-serif;
}
</style>
