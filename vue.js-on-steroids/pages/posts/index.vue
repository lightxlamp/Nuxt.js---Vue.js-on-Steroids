<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>

export default {
  asyncData(context) {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
         resolve({
            loadedPosts: [
                {
                id: "1",
                title: "First Post",
                previewText: "This is our first post!",
                thumbnail:
                    "https://static.pexels.com/photos/270348/pexels-photo-270348.jpeg"
                },
                {
                id: "2",
                title: "Second Post",
                previewText: "This is our second post!",
                thumbnail:
                    "https://static.pexels.com/photos/270348/pexels-photo-270348.jpeg"
                }
            ]
            });
        }, 1000);
      })
      .then(data => {
      return data
    })
    .catch(e => {
        context.console.error(e);
        
    });
  },
  created() {
    this.$store.dispatch('setPosts', this.loadedPost)
  }
};
</script>


<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
