<template>
  <article>
    <NuxtLink :to="{ name: 'blog-slug', params: { slug: slug } }">
      <header class="header">
        <h3 class="title">{{ title }}</h3>
        <small>{{ formatDate(postDate) }}</small>
      </header>
      <section class="content">
        {{ description }}
      </section>
    </NuxtLink>
  </article>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  props: {
    title: {
      type: String,
    },
    postDate: {
      type: String,
    },
    readingTime: {
      type: String,
    },
    description: {
      type: String,
    },
    slug: {
      type: String,
    },
  },
  setup() {
    const formatDate = (date: string) => {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }

    return { formatDate }
  },
})
</script>

<style lang="postcss" scoped>
article {
  font-family: 'Merriweather', 'Georgia', sans-serif;
}

.title {
  font-weight: 900;
  font-size: 1.4rem;
  margin-bottom: 0.3rem;
}

small {
  font-weight: 500;
}

.content {
  font-family: 'Merriweather', 'Georgia', sans-serif;
  font-size: 1rem;
  font-weight: 500;
}
</style>
