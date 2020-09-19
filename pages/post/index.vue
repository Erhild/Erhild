<template>
  <div>
    <Post
      v-for="(article, index) in articles"
      :key="index"
      :title="article.title"
      :post-date="article.createdAt"
      :description="article.description"
      :slug="article.slug"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent, useAsync, useContext } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const { params, $content } = useContext()
    const articles = useAsync(() =>
      $content('articles', params.value.slug).fetch()
    )
    console.log('setup -> articles', articles)
    return {
      articles,
    }
  },
})
</script>
