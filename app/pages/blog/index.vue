<template>
  <section class="blog">
  <div class="x">
    <div class="py-8 md:py-16 text-center">
      <h1 class="text-2xl md:text-3xl lg:text-4xl xl:text-6xl">Events</h1>
      <h2 class="text-base md:text-lg lg:text-xl xl:text-2xl">
        See how we have fun
      </h2>
    </div>
    <div class="flex flex-wrap md:-mx-4 pb-20">
      <div v-for="(post, index) in posts" :key="index" class="w-full md:w-1/2 my-4 px-4">
        <div class="post" style="box-shadow: none !important">
          <nuxt-link :to="`/blog/${post.slug}`">
            <img
              :alt="post.title"
              class="w-full"
              :src="post.featuredImage || 'https://source.unsplash.com/random/640x340'"
            />
            <div class="p-6 bg-white">
              <h2 class="text-2xl mb-2 cl-black">{{ post.title }}</h2>
            </div>
          </nuxt-link>
        </div>
      </div>
    </div>
    <Pagination v-if="totalPages > 1" :current-page="currentPage" :total-pages="totalPages" />
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
      title: 'Blog',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Blog index',
        },
      ],
    };
  },
})
export default class BlogIndex extends Vue {
  currentPage!: number;

  totalPages!: number;

  posts: Post[] = [];

  async asyncData({ params, store }) {
    const page: number = params.page ? parseInt(params.page, 10) : 1;
    const { perPage }: { perPage: number } = store.state;
    const range = page * perPage;

    const posts = store.state.posts.filter((post, index) => {
      const indexPage = index + 1;
      return range - perPage < indexPage && indexPage <= range;
    });

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
