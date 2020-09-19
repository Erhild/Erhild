<template>
  <article>
    <nuxt-content :document="article" />
  </article>
</template>

<script lang="ts">
import { defineComponent, useAsync, useContext } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const { params, $content } = useContext()
    const article = useAsync(() =>
      $content('articles', params.value.slug).fetch()
    )

    const formatDate = (date: string) => {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
    return {
      article,
      formatDate,
    }
  },
})
</script>
