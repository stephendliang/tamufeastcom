<template>
  <section class="home">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col md:flex-row items-center bg-fit" v-bind:style="{ backgroundImage: 'url(' + header + ')' }">
      <div class="x">
        <div class="flex flex-col w-full xl:w-3/5 justify-center lg:items-start overflow-y-hidden">
          <div v-html="$md.render(welcomeText)" class="home__welcome markdown" style="color:#fff" />
          <div class="mb-12 xl:mb-0">

          </div>
        </div>
        <div class="flex flex-col w-full xl:w-2/5">
        </div>
      </div>
    </div>
    
    <div class="w100 pdstd rel bg- g1 spotlight pt128 pb32">
      <div class="rel">
        <div class="bsbx w100 mt3 rel">
          <div class="w100 w home-swap mt6 mat " style="max-width: 760px">
            <h3 class="w6 big mb0 mt1 f45 tc">Review Critiques.</h3>
            <p class="f21 mt24 w4 tc">See how other contributors feel about your content in a qualitative and quantatative light.</p>
          </div>


          <ul class="L gg50 gp50 mt128 w100 mra ">

            <li class="gp50 y">
              <div class="ml20">
                <h4 class="f15 mt10 w6  bl-std mt1 f19 mb0">Highly accurate ratings</h4>
                <p class="mt16">Machine learning algorithms will detect spammy ratings and discard them.</p>
              </div>
            </li>

            <li class="gp50 y">
              <svg class="mt12" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="36px"
                 height="36px" viewBox="0 0 36 36" style="overflow:visible;enable-background:new 0 0 36 36;" xml:space="preserve">
              <g>
                <path class="st0" d="M27.3,36H8.7C3.9,36,0,32.1,0,27.3V8.7C0,3.9,3.9,0,8.7,0h18.7C32.1,0,36,3.9,36,8.7v18.7
                  C36,32.1,32.1,36,27.3,36z"/>
              </g>
              <g>
                <path fill="white" d="M27.2,14.2h-2.4v5.5c0,1.3-1.1,2.4-2.4,2.4H18l-2.8,2.4h5.3l3.7,3.1c0.1,0.1,0.2,0.1,0.3,0.1
                  c0.1,0,0.1,0,0.2,0c0.1-0.1,0.2-0.2,0.2-0.4v-2.8h2.4c0.4,0,0.8-0.4,0.8-0.8V15C28,14.6,27.6,14.2,27.2,14.2z"/>
                <path fill="white" d="M22.5,10.3H9.8c-0.4,0-0.8,0.4-0.8,0.8v8.7c0,0.4,0.4,0.8,0.8,0.8h2.4v3.6c0,0.2,0.1,0.3,0.2,0.4
                  c0.1,0,0.1,0,0.2,0c0.1,0,0.2,0,0.3-0.1l4.6-3.9h5c0.4,0,0.8-0.4,0.8-0.8v-8.7C23.2,10.6,22.9,10.3,22.5,10.3z"/>
              </g>
              </svg>
              <div class="ml20">
                <h4 class="f15 mt10 w6  bl-std mt1 f19 mb0">Detailed commenting</h4>
                <p class="mt16">We encourage raters to have high-quality comments on how to improve.</p>
              </div>
            </li>

            <li class="gp50 y">
              <!-- Generator: Adobe Illustrator 24.2.3, SVG Export Plug-In  -->
<svg class="mt12" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="36px"
   height="36px" viewBox="0 0 36 36" style="overflow:visible;enable-background:new 0 0 36 36;" xml:space="preserve">
<style type="text/css">
  .st1{fill:#FFFFFF;}
</style>
<defs>
</defs>
<g>
  <path class="st0" d="M27.3,36H8.7C3.9,36,0,32.1,0,27.3V8.7C0,3.9,3.9,0,8.7,0h18.7C32.1,0,36,3.9,36,8.7v18.7
    C36,32.1,32.1,36,27.3,36z"/>
</g>
<g>
  <path fill="white" d="M8.7,16.6c0.2,0,0.4-0.1,0.5-0.2l5.9-5.9l5.2,5.2c0.3,0.3,0.7,0.3,1,0l6.4-6.4c0.3-0.3,0.3-0.7,0-1
    c-0.3-0.3-0.7-0.3-1,0c0,0,0,0,0,0l-5.9,5.9l-5.2-5.2c-0.3-0.3-0.7-0.3-1,0l-6.4,6.4c-0.3,0.3-0.3,0.7,0,1
    C8.3,16.5,8.5,16.6,8.7,16.6z"/>
  <path fill="white" d="M19.8,21.6h2.1c0.2,0,0.4,0.2,0.4,0.4v5.7c0,0.2-0.2,0.4-0.4,0.4h-2.1c-0.2,0-0.4-0.2-0.4-0.4v-5.7
    C19.4,21.7,19.6,21.6,19.8,21.6z"/>
  <path fill="white" d="M25.5,15.1h2.1c0.2,0,0.4,0.2,0.4,0.4v12.1c0,0.2-0.2,0.4-0.4,0.4h-2.1c-0.2,0-0.4-0.2-0.4-0.4V15.5
    C25.1,15.3,25.3,15.1,25.5,15.1z"/>
  <path fill="white" d="M14.1,15.1h2.1c0.2,0,0.4,0.2,0.4,0.4v12.1c0,0.2-0.2,0.4-0.4,0.4h-2.1c-0.2,0-0.4-0.2-0.4-0.4V15.5
    C13.7,15.3,13.9,15.1,14.1,15.1z"/>
  <path fill="white" d="M8.4,21.6h2.1c0.2,0,0.4,0.2,0.4,0.4v5.7c0,0.2-0.2,0.4-0.4,0.4H8.4C8.2,28,8,27.8,8,27.6v-5.7
    C8,21.7,8.2,21.6,8.4,21.6z"/>
</g>
</svg>

              <div class="ml20">
                <h4 class="f15 mt10 w6  bl-std mt1 f19 mb0">Quick &amp; plentiful results</h4>
                <p class="mt16">Machine learning algorithms will detect spammy ratings and discard them..</p>
              </div>
            </li>

            <li class="gp50 y">
              <!-- Generator: Adobe Illustrator 24.2.3, SVG Export Plug-In  -->
<svg class="mt12" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="36px"
   height="36px" viewBox="0 0 36 36" style="overflow:visible;enable-background:new 0 0 36 36;" xml:space="preserve">
<g>
  <path class="st0" d="M27.3,36H8.7C3.9,36,0,32.1,0,27.3V8.7C0,3.9,3.9,0,8.7,0h18.7C32.1,0,36,3.9,36,8.7v18.7
    C36,32.1,32.1,36,27.3,36z"/>
</g>
<g>
  <path fill="white" d="M18.5,23.1c-2.1,0-2.9-0.9-3-2.1h-2.2c0.1,2.2,1.8,3.4,3.7,3.8V27h3v-2.1c2-0.4,3.5-1.5,3.5-3.6
    c0-2.8-2.4-3.8-4.7-4.4s-3-1.2-3-2.1c0-1.1,1-1.9,2.7-1.9c1.8,0,2.4,0.9,2.5,2.1h2.2c-0.1-1.7-1.1-3.3-3.2-3.8V9h-3v2.2
    c-1.9,0.4-3.5,1.7-3.5,3.6c0,2.3,1.9,3.5,4.7,4.1c2.5,0.6,3,1.5,3,2.4C21.2,22,20.7,23.1,18.5,23.1z"/>
</g>
</svg>

              <div class="ml20">
                <h4 class="f15 mt10 w6  bl-std mt1 f19 mb0">Cheap input costs</h4>
                <p class="mt16">You won't have to rate any other users' pictures if you buy credits (40 credits for $2).</p>
              </div>
            </li>

          </ul>
        </div>
      </div>
    </div>












    <div class="bg- pdst pt128 pb96 " style="background: #;">
      <div class=" narrow c y z">
        <div class="w100 mt24 bsbx y z v-mlg">
            <div style="max-width: 567px">
              <h3 class="mt0 w6">Ready to get started?</h3>
              <p class="mt1 cl-swap w4">We're currently not done setting up the backend currently, but you can sign up to receive updates when it's done.</p>
            </div>
            <ul class="L y pl mt25">
              <li class="mr25p">
                <a class="cl-swap big f19 rel btn alt bg-blue0 w" href="/signup.html">
                  <span class="">Sign up</span>
                  <svg width="10" height="10" viewBox="0 0 10 10" aria-hidden="true"><path stroke="#fff" stroke-width="2" fill="none" d="M1 1l4 4-4 4"></path></svg>
                </a>
              </li>
              <li class="ml24">
                <a class="cl-swap big f19 rel btn blue bg-blue0 w" href="/faq.html">
                  <span class="">View FAQ</span>
                </a>
              </li>
            </ul>
        </div>
      </div>
    </div>
    
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component({
  // Called to know which transition to apply
  transition() {
    return 'slide-left';
  },
})
export default class Home extends Vue {
  welcomeText = settings.welcomeText;
  header = settings.header;

  get posts(): Post[] {
    return this.$store.state.posts;
  }

  isSignedUp = false;

  form = {
    email: '',
  };

  encode(data): string {
    return Object.keys(data)
      .map((key) => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`)
      .join('&');
  }

  validEmail(email): boolean {
    // eslint-disable-next-line
    const re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
    return re.test(email);
  }

  async handleSubmit(): Promise<void> {
    if (!this.validEmail(this.form.email)) {
      this.$refs.emailInput.focus();
      return;
    }

    try {
      await fetch('/', {
        method: 'POST',
        headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
        body: this.encode({ 'form-name': 'signups', ...this.form }),
      });

      this.isSignedUp = true;
    } catch (error) {
      console.error(error);
    }
  }
}
</script>
