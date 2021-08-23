<template>
  <footer class="footer py-4">
      <div class="container">
          <div class="row align-items-center">
              <div class="col-lg-4 text-lg-start"></div>
              <div class="col-lg-4 my-3 my-lg-0">
                <a class="btn btn-social mx-2" href="https://twitter.com/tamufeast">
                  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 512 512"><title>logo-twitter</title><g fill="#212121"><path d="M496 109.5a201.8 201.8 0 0 1-56.55 15.3 97.51 97.51 0 0 0 43.33-53.6 197.74 197.74 0 0 1-62.56 23.5A99.14 99.14 0 0 0 348.31 64c-54.42 0-98.46 43.4-98.46 96.9a93.21 93.21 0 0 0 2.54 22.1 280.7 280.7 0 0 1-203-101.3A95.69 95.69 0 0 0 36 130.4c0 33.6 17.53 63.3 44 80.7A97.5 97.5 0 0 1 35.22 199v1.2c0 47 34 86.1 79 95a100.76 100.76 0 0 1-25.94 3.4 94.38 94.38 0 0 1-18.51-1.8c12.51 38.5 48.92 66.5 92.05 67.3A199.59 199.59 0 0 1 39.5 405.6a203 203 0 0 1-23.5-1.4A278.68 278.68 0 0 0 166.74 448c181.36 0 280.44-147.7 280.44-275.8 0-4.2-.11-8.4-.31-12.5A198.48 198.48 0 0 0 496 109.5z"></path></g></svg>
                </a>
                <a class="btn btn-social mx-2" href="https://instagram.com/tamufeast" style="margin-left:20px">
                  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 512 512"><title>logo-instagram</title><g fill="#212121"><path d="M349.33 69.33a93.62 93.62 0 0 1 93.34 93.34v186.66a93.62 93.62 0 0 1-93.34 93.34H162.67a93.62 93.62 0 0 1-93.34-93.34V162.67a93.62 93.62 0 0 1 93.34-93.34h186.66m0-37.33H162.67C90.8 32 32 90.8 32 162.67v186.66C32 421.2 90.8 480 162.67 480h186.66C421.2 480 480 421.2 480 349.33V162.67C480 90.8 421.2 32 349.33 32z"></path><path d="M377.33 162.67a28 28 0 1 1 28-28 27.94 27.94 0 0 1-28 28z"></path><path d="M256 181.33A74.67 74.67 0 1 1 181.33 256 74.75 74.75 0 0 1 256 181.33m0-37.33a112 112 0 1 0 112 112 112 112 0 0 0-112-112z"></path></g></svg>
                </a>
              </div>
              <div class="col-lg-4 text-lg-end">
                  <nuxt-link :to="`/${page.slug}`"
          v-for="(page, index) in pages"
          :key="index"
          class="link-dark text-decoration-none me-3" href="#!"{{ page.title }}</nuxt-link>
              </div>
          </div>
      </div>
  </footer>
        
</template>


<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
@Component
export default class Footer extends Vue {
  get pages(): Page[] {
    return this.$store.state.pages;
  }
}
</script>



<style lang="scss">
.footer {
  border-top: 1px solid #fafbff
}
</style>
