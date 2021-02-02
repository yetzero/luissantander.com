<template>
  <Layout>
    <g-link to="/projects">&lt; All projects</g-link>
    <h1>{{ $page.project.title }}</h1>
    <p>{{ $page.project.description }}</p>
    <div class="project-assets p-20 text-lg">
      <figure v-for="asset in $page.project.assets">
        <g-image :src="asset.image.asset.url" />
        <legend v-if="asset.caption">{{ asset.caption }}</legend>
      </figure>
    </div>
  </Layout>
</template>

<page-query>
query ($id: ID!) {
  project: sanityProject(id: $id) {
    id
    title
    description
    assets {
      image {
        asset {
          url
        }
      }
      caption
    }
    category {
      title
    }
    softwareUsed {
      name
    }
  }
}
</page-query>
