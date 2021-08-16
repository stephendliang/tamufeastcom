<template>
  <section class="home">
    <div class="py-24 md:py-36 mx-auto flex flex-wrap flex-col md:flex-row items-center bg-fit" v-bind:style="{ backgroundImage: 'url(' + header + ')' }">
      <div class="x">
        <div class="">
          <h2 class="" style="color:#fff;font-size:45px;font-weight:600;text-align:center;text-transform:uppercase">{{ taglineText }} </h2>
          <p class=" " style="color:#fff;font-size:22px;font-weight:600;text-align:center;text-transform:uppercase;text-decoration:italic">{{ subtagText }} </p>
        </div>
      </div>
    </div>
    
    
    <div>
      <div class="x">
        <div class="flex flex-col w-full xl:w-3/5 justify-center lg:items-start overflow-y-hidden">
          <div v-html="$md.render(welcomeText)" class="home__welcome markdown tc"/>
        </div>
        <div class="flex flex-col w-full xl:w-2/5">
        </div>
      </div>
    </div>
    










    <div class="bg- pdst pt128 pb96 " style="padding: 120px 0 80px">
      <div class="x c y z">
        <div style="max-width: 567px">
          <h3 class="mt0 w6">Ready to get started?</h3>
          <p class="mt1 cl-swap w4">We're currently not done setting up the backend currently, but you can sign up to receive updates when it's done.</p>
        </div>
        <ul class="L y pl mt25">
          <li class="mr25p">
            <a class="cl-swap big f19 rel button alt bg-blue0 w" href="/signup.html">
              <span class="">Sign up</span>
              <svg width="10" height="10" viewBox="0 0 10 10" aria-hidden="true"><path stroke="#fff" stroke-width="2" fill="none" d="M1 1l4 4-4 4"></path></svg>
            </a>
          </li>
          <li class="ml24">
            <a class="cl-swap big f19 rel button blue bg-blue0 w" href="/faq.html">
              <span class="">View FAQ</span>
            </a>
          </li>
        </ul>
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
  subtagText = settings.subtagText;
  taglineText = settings.taglineText;
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
