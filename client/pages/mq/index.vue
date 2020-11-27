<template>
  <table 
    style="width:100%;" 
    border="1">
    <tr>
      <th>MQ Server IP</th>
      <th>MQ Type</th>
      <th>MQ 동기화 설정</th>
    </tr>
    <tr>
      <td>노트북</td>
      <td>001</td>
      <td><input 
        type="checkbox" 
        name="check1"></td>
    </tr>
    <tr>
      <td>조정실</td>
      <td>002</td>
      <td><input 
        type="checkbox" 
        name="check2"></td>
    </tr>
    <tr>
      <td>외부노트북</td>
      <td>003</td>
      <td><input 
        type="checkbox" 
        name="check3"></td>
    </tr>
  </table>
</template>

<script>
export default {
  name: 'Clinet',
  props: {
    id: {
      type: Number,
      required: true
    },
    isAdmin: {
      type: Boolean,
      required: true
    },
    thumbnail: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    }
  },
  computed: {
    ellipseContent() {
      const ellipseText =
        this.content.length < 55
          ? this.content
          : this.content.slice(0, 50) + '...'
      return ellipseText
    }
  }
}
</script>

<style lang="sass" scoped>
	.page-single-post
		padding: 30px
		text-align: center
		box-sizing: border-box

	.post
		width: 100%

	.post-title
		margin: 0

	.post-info
		display: flex
		justify-content: center
		align-items: center
		flex-direction: column
		box-sizing: inherit
		border-bottom: 1px solid #ccc
		padding: 10px

	.post-data,
	.post-author
		margin: 0 10px
		color: #9a9a9a

	.post-feedback a
		padding:
			left: 5px
			right: 5px
		color: #46b784
		text-decoration: none
		transition: color 0.4s ease
		&:hover,
		&:active
			color: darken(#46b784, 20%)


	@media (min-width: 768px)
		.post
			width: 600px
			margin: auto

		.post-info
			flex-direction: row
</style>
