<template>
  <layout>

    <MetaInfo
      :pageTitle = "$page.post.title"
      :pageDescription = "$page.post.description"
      :pageImage = "$page.post.cover_image.src"
      :pageImageHeight = "'576'"
    />

    <div class="layout__title blog_title">
      <h1>{{ $page.post.title }}</h1>
    </div>

    <div class="layout">
      <PostMeta :post="$page.post" />
    </div>

    <Abstract v-if="$page.post.abstract" :text="$page.post.abstract" :className="'post_abstract'"/>

    <div class="post__header animate-inside" v-in-viewport.once>
        <g-image :alt="$page.post.title" v-if="$page.post.cover_image" :src="$page.post.cover_image"/>
    </div>


    <section class="post layout layout__text">
       <VueRemarkContent />
    </section>

    <PostRelated v-if="$page.post.related.length > 0" />
       
  </layout>
</template>


<static-query>
  query {
    metadata {
      siteName,
      siteDescription
    }
  }
</static-query>


<page-query>
query($id: ID!) {
  post(id: $id) {
    title
    cover_image (width: 2000, quality: 100)
    description
    path
    date (format: "MMMM D, YYYY")
    content
    related
    abstract
    tags {
      id
      title
      path
    }
  }
  allPost{
    edges {
      node {
        title
        cover_image (width: 2000, quality: 100)
        path
      }
    }
  }
}

</page-query>


<script>

  export default {

    components: {
      MetaInfo: () => import('~/components/MetaInfo.vue'),
      PostMeta: () => import('~/components/PostMeta.vue'),
      // PostTags: () => import('~/components/PostTags.vue'),
      PostCard: () => import('~/components/PostCard.vue'),
      PostRelated: () => import('~/components/PostRelated.vue'),
      Abstract: () => import('~/components/TextAbstract.vue'),
    }

  }

</script>


<style lang="scss">
  .post {
    padding: var(--space);
    text-align: left;
    font-weight: 400;

    &__header {
      margin-top: var(--space-text);
      max-width: 1400px;
      margin-left: auto;
      margin-right: auto;

      img {
        display: block;
        max-width: 100%;
        margin-left: auto;
        margin-right: auto;
      }
    }

    strong, b {
      background-color: #f8ffb5;
    }
  }
</style>

