<template lang="pug">
.page-home
  // loadedPosts 데이터를 
  // PostList 컴포넌트 posts 속성으로 전달
  post-list(:posts="loadedPosts")
</template>


<script>
import PostList from '@/components/Posts/PostList'

export default {
  components: { PostList },
  data() {
    return {
      // PostList 컴포넌트에 넘겨 줄 데이터
      loadedPosts: [
        {
          id: 1,
          title: '클라이언트 설정',
          thumbnail: '//goo.gl/mJ5Vsy',
          content: '1'
        },
        {
          id: 2,
          title: '라우터 설정',
          thumbnail: '//goo.gl/HoiVkE',
          content: '2'
        },
        {
          id: 3,
          title: '녹화기 설정',
          thumbnail: '//goo.gl/mJ5Vsy',
          content: '3'
        },
        {
          id: 4,
          title: 'MQ 설정',
          thumbnail: '//goo.gl/HoiVkE',
          content: '4'
        }
      ]
    }
  }
}
</script>


<style lang="sass" scoped>
@import "~assets/styles/config"

a
  text-decoration: none
  color: darken($color, 20%)
  transition: all 0.4s ease
  &:hover .post-content,
  &:active .post-content
    background-color: rgba($color, 0.26)

@media (min-width: 768px)
  .intro h1
    font-size: 2rem
</style>
