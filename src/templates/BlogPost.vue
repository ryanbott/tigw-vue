<template lang="pug">
  <Layout>
    <div class="article">
      <h1>{{ $page.blogPost.title }}</h1>
      <span>{{ $page.blogPost.date }}</span>
      <img :src="$page.blogPost.fields.image"/>
      <div class="content" v-html="$page.blogPost.content" />
    </div>
  </Layout>
</template>

<script>
  export default {
    metaInfo () {
      return {
        title: this.$page.blogPost.title
      }
    }
  }
</script>

<page-query>
  query BlogPost ($path: String!) {
    blogPost (path: $path) {
      title
      date (format: "D MMMM, YYYY")
      content
      fields {
        image
      }
    }
  }
</page-query>

<style>
  /* .header {
    margin-bottom: 70px;
  } */

  .article {
    margin-top: 1.5rem;
  }

  .article h1 {
    font-size: 4rem;
  }

  .article img {
    width: 100%;
    border-radius: 5px;
  }

  .article a {
    color: #4dba87;
    text-decoration: underline;
  }

  .article a:hover {
    text-decoration: none;
  }

  .article span {
    font-size: 1.4rem;
    margin-bottom: 2rem;
  }

  .article ol, .article ul {
    list-style-position: outside;
  }

  .article ul {
    list-style: disc;
    padding-left: 20px;
  }

  .article .content p:first-child {
    margin-top: 15px;
  }

  .article .content p {
    margin-top: 0;
    margin-bottom: 10px;
    line-height: 1.5;
  }
</style>
