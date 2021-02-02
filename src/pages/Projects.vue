<template>
  <Layout>
    <h1>This is the projects page</h1>
    <div class="grid grid-flow-row grid-cols-3 gap-2">
      <g-link
        v-for="project in $page.projects.edges"
        class="project-card"
        :key="project.node.id"
        :to="project.node.path"
      >
        <p>{{ project.node.title }}</p>
        <p>{{ project.node.description }}</p>
        <g-image :src="project.node.coverImage.asset.url" />
      </g-link>
    </div>
  </Layout>
</template>

<page-query>
query allSanityProject ($page: Int) {
  projects: allSanityProject (sortBy: "title", order: DESC, perPage: 6, page: $page) @paginate {
    totalCount
    pageInfo {
      totalPages
      currentPage
    }
    edges {
      node {
        title
        description
        slug
        path
        coverImage {
          asset {
            url
          }
        }
      }
    }
  }
}
</page-query>

<script>
export default {};
</script>

<style scoped></style>
