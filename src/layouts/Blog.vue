<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/" class="site-title">{{ $static.metaData.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about">About</g-link>
        <g-link class="nav__link" to="/team">Team</g-link>
        <!-- <g-link class="nav__link" to="/blog">Blog</g-link> -->
      </nav>
    </header>
    <slot/>
  </div>
</template>


<script>
export default {
  metaInfo: {
    title: 'About us'
  }
}
</script>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style>
@import url("https://cdnjs.cloudflare.com/ajax/libs/github-markdown-css/3.0.1/github-markdown.min.css");


body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.site-title {
  text-decoration-line: none;
  color: white;
}

.site-title:hover {
  color: yellow;
}

.nav__link {
  margin-left: 20px;
}

.markdown-body {
		box-sizing: border-box;
		min-width: 200px;
		max-width: 980px;
		margin: 0 auto;
		padding: 45px;
        color: white;
	}

	@media (max-width: 767px) {
		.markdown-body {
			padding: 15px;
		}
	}
</style>

