<template lang="pug">
  <Layout class="home">
    <ul>
      <li v-for="{ node } in $page.allBlogPost.edges" :key="node._id">
        <router-link :to="node.path">
          <h2 v-html="node.title"/>
        </router-link>
        <span v-html="node.date"/>
        <div v-html="node.fields.description"/>
      </li>
    </ul>
  </Layout>
</template>

<page-query>
  query Home ($page: Int) {
    allBlogPost (page: $page) {
      edges {
        node {
          _id
          title
          date (format: "D MMMM, YYYY")
          fields {
            description
          }
          path
        }
      }
    }
  }
</page-query>

<style lang="sass" scoped>
  .home
    max-width: 90rem;
    background: var(--light-bg);
    margin: auto;
</style>
