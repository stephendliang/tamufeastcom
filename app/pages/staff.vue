<template>
  <section class="blog">
    <div class="x">
      <div class="py-8 md:py-16 text-center">
        <h1 class="text-lg md:text-xl lg:text-4xl xl:text-6xl">Staff members</h1>
        <h2 class="text-base md:text-lg lg:text-xl xl:text-2xl">
        Here's who we work with.
        </h2>
      </div>

      <div class="flex flex-wrap md:-mx-4 pb-20">
        <div v-for="(post, index) in posts" :key="index" class="w-full">
          <div class="post">
            <h3 class="text-base font-light">{{ post.name }}</h3>
            <p class="text-base font-light">{{ post.content }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import { MetaInfo } from 'vue-meta';
const Pagination = () => import('@/components/commons/pagination.vue');
@Component({
  components: {
    Pagination,
  },
  head(): MetaInfo {
    return {
      title: 'Staff',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Blog index',
        },
      ],
    };
  },
})export default class BlogIndex extends Vue {
  currentPage!: number;
  totalPages!: number;
  posts: Post[] = [];
  async asyncData({ params, store }) {
    const page: number = params.page ? parseInt(params.page, 10) : 1;
    const { perPage }: { perPage: number } = store.state;
    const range = page * perPage;
    const posts = store.state.posts
    console.log(posts)
    return {
      currentPage: page,
      totalPages: Math.ceil(store.state.posts.length / perPage),
      posts: posts || [],
    };
  }
}
</script>

<style lang="scss">
.blog {
  .post {
    @apply shadow-md;
    transition: all 0.2s cubic-bezier(0.64, 0, 0.35, 1);
    &:hover {
      @apply shadow-xl;
    }
  }
}
</style>
