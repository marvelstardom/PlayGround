<template>
  <Layout>
    
    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/play.png" width="135" />
    
    <h1>Hello, Developers!</h1>

    <h3>Welcome To PlayGround! </h3>  
    
    <h3> We are happy to have you here.</h3>
   
    <h3>
      Connect with developers across the world.
    </h3>

    <h2>Manual Blogroll</h2>

    <ul>
      <li><g-link to="/blog-html/blog-post-one" class="link">Dinner Night</g-link> </li>
      <li><g-link to="/blog-html/blog-post-two" class="link">Be Different</g-link> </li>
    </ul>

    <h2>Automatic Blogroll</h2>

    <ul>
      <li v-for="post in $page.posts.edges" :key="post.id">
        <g-link :to="post.node.path" class="link">{{ post.node.title }}</g-link>
      </li>
    </ul>

    <p class="home-links">
      <a href="https://gridsome.org/docs" target="_blank" rel="noopener">Gridsome Docs</a>
      <a href="https://github.com/gridsome/gridsome" target="_blank" rel="noopener">GitHub</a>
    </p>

  </Layout>
</template>

<page-query>
query Posts {
  posts: allPost {
    edges {
      node {
        id,
        title,
        path
      }
    }
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    title: 'Developers PlayGround!'
  }
}
</script>

<style scoped>
.Layout {
  max-height: -webkit-fill-available;
}
.home-links a {
  margin-right: 1rem;
}

h1 {
  color: yellow;
}

.link{
   color: yellow;
}
</style>
