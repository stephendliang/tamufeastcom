<template>
  <header class="flex items-center" style="background:transparent;position:absolute;width:100%;padding:2em 0;">
    <div class="x y">
      <div class="header__logo">
        <nuxt-link to="/" style="color: #fff;font-weight:600;font-size:24px">
          {{ logo }}
        </nuxt-link>
      </div>

      <nav class="nav ml-auto">
        <ul class="flex flex-row items-center sm:mt-4 sm:pt-4 md:mt-0 md:pt-0">
        <!--
          <li>
            <nuxt-link to="/blog" class="block font-medium px-4 py-1 md:p-2 lg:px-4">
              Blog
            </nuxt-link>
          </li>-->

          <li
            v-for="(page, index) in pages"
            :key="index"
            class="block font-medium py-1"
            style="color:#fff;margin-left:20px"
          >
            <nuxt-link :to="`/${page.slug}`">{{ page.title }}</nuxt-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component
export default class Header extends Vue {
  get pages(): Page[] {
    return this.$store.state.pages;
  }

  logo = settings.logo;
}
</script>

<style lang="scss">
.nav {
  ul li > a {
    &.nuxt-link-active {
      @apply font-bold;
    }
  }
}
</style>
