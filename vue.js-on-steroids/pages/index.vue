<template>
  <div class="container">
    <section class="intro">
      <h1>Get the latest tech news</h1>
    </section>

    <section class="featured-posts">    
      <PostPreview 
        id="1"
        thumbnail="https://www.acq-intl.com/wp-content/uploads/2020/01/tech-cruve.jpg"
        title="Hey Stas"
        previewText="This is my first Post"
      />   
      
      <PostPreview 
        id="2"
        thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSlOzmaKIcR2fnhzTNA0fRuV2Eoch8au4nUaIUthUqsjx5VVB1E&usqp=CAU"
        title="Dynamic second post"
        previewText="Dynamically generated second post"
      /> 
      
      <PostPreview 
        id="3"
        thumbnail="https://m.economictimes.com/thumb/msid-74211022,width-1200,height-900,resizemode-4,imgsize-743396/quantum-computing.jpg"
        title="Dynamic third post"
        previewText="Dynamically generated third post"
      />
    </section>
  <!--  <nuxt-link to="/users">Users</nuxt-link> catches all clicks and ensures that no request is sent -->
  </div>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview'

export default {
  components: {
    PostPreview
  }
}
</script>

<style scoped>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~assets/images/original.jpg'); /* this will be processed by webpack */
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>