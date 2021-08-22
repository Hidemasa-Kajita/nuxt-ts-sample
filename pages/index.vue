<template>
  <div>
    {{ posts }}
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  async asyncData(context) {
    const posts = await context.$axios.$get('/posts')
    return { posts }
  },
})
</script>
