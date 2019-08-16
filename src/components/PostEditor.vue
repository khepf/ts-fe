<template>
  <form @submit.prevent="save">
    <div class="form-group">
      <textarea 
      name="" 
      id="" 
      cols="30" 
      rows="10" 
      class="form-input"
      v-model="text"></textarea>
    </div>
    <div class="form-actions">
      <button class="btn-blue">Submit Post</button>
    </div>
  </form>
</template>

<script>
// import sourceData from '@/data'
export default {
  props: {
    threadId: {
      required: true
    }
  },
  data () {
    return {
      text: ''
    }
  },
  methods: {
    save () {
      const postId = 'greatpost' + Math.random()
      const post = {
        text: this.text,
        publishedAt: Math.floor(Date.now() / 1000),
        threadId: this.threadId,
        userId: 'ALXhxjwgY9PinwNGHpfai6OWyDu2',
        '.key': postId
      }
      // this.$set(sourceData.posts, postId, post)
      // this.$set(this.thread.posts, postId, postId)
      // this.$set(sourceData.users[post.userId].posts, postId, postId)
      this.text = ''

      this.$emit('save', {post})
    }
  }
}
</script>

<style scoped>

</style>