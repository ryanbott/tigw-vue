<template lang="pug">
  Layout.home
    .show-index
      ul
        <li v-for="{ node } in $page.allBlogPost.edges" :key="node._id">
          <router-link :to="node.path">
            <h2 v-html="node.title"/>
          </router-link>
          <span v-html="node.date"/>
          <div v-html="node.fields.description"/>
        </li>
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
    margin: auto;

    ul
      padding: 2rem;

      li
        border-bottom: 1px solid var(--orange1);

    h2
      font-size: 2rem;
      font-weight: 500;
</style>
