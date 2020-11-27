<template lang="pug">
.page-home
  post-list
</template>

<script>
import PostList from '@/components/Posts/PostList'

export default {
  components: { PostList }
}
</script>

<style lang="sass" scoped>
.page-title
  margin-bottom: 0
  font-family: Changa, Sans-Serif
  letter-spacing: -0.03em

p
  margin-top: 0
  color: rgba(#000, 0.5)
  font-size: 13px
  letter-spacing: -0.06em
</style>
