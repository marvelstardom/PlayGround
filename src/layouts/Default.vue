<template>
  <div class="layout">
    <div class="nav-head">
    <header class="header">
      <strong>
        <g-link to="/"><h2 class="site-title">{{ $static.metaData.siteName }}</h2></g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about">About</g-link>
        <g-link class="nav__link" to="/team">Team</g-link>
        <!-- <g-link class="nav__link" to="/blog">Blog</g-link> -->
      </nav>
    </header>
    </div>
    <slot/>
  </div>
</template>

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
  background-image: linear-gradient(120deg,rgba(82, 75, 79, 0.4),rgba(255,0,150,0.4)),url('../Playground-1.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  opacity: 1;
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
  color: white;
  height: auto;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;

}

/* .nav-head {
  background-color: aqua;
  width: 100%;
} */

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.site-title {
  text-decoration: none;
  color: white;
}

.site-title:hover {
  color: yellow;
}

.nav__link {
  margin-left: 20px;
  text-decoration: none;
  color: white;
}
.nav__link:hover {
  color: yellow;
}

.markdown-body {
		box-sizing: border-box;
		min-width: 200px;
		max-width: 980px;
		margin: 0 auto;
		padding: 45px;
	}

	@media (max-width: 767px) {
		.markdown-body {
			padding: 15px;
		}
	}
</style>
