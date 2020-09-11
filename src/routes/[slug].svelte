<script context="module">
  export async function preload({ params, query }) {
    const res = await this.fetch(`${params.slug}.json`);
    const data = await res.json();

    if (res.status === 200) {
      return { post: data };
    } else {
      this.error(res.status, data.message);
    }
  }
</script>

<script>
  import { _, locale, locales, dictionary } from "svelte-i18n";

  export let post;
</script>

<div class="px-4 py-16 overflow-hidden bg-white xl:py-36 sm:px-6 lg:px-8">
  <div class="mx-auto max-w-max-content lg:max-w-7xl">
    <div class="relative z-10 mb-8 md:mb-2 md:px-6">
      <div class="text-base max-w-prose lg:max-w-none">
        <p
          class="font-semibold leading-6 tracking-wide uppercase text-mcorange2">
          {$_('rights.subtitle')}
        </p>
        <h1
          class="mt-2 text-3xl font-extrabold leading-8 tracking-tight text-mcblack sm:text-5xl sm:leading-10">
          {post.country}
        </h1>
        <p class="pt-5">
          {@html $_('rights.body')}
        </p>
      </div>
    </div>
    <div class="relative">
      <div class="relative md:bg-white md:p-6">
        <div class="mb-8 lg:grid lg:grid-cols-2 lg:gap-6">
          <div class="mb-6 prose prose-lg text-color3 lg:max-w-none lg:mb-0">
            <h2
              class="py-3 font-semibold leading-6 tracking-wide uppercase sm:text-xl text-mcorange2">
              {post.laws[0].title}
            </h2>
            <p>
              {@html post.laws[0].content}
            </p>
          </div>
          <div class="prose prose-lg text-color3">
            <h2
              class="py-3 font-semibold leading-6 tracking-wide uppercase sm:text-xl text-mcorange2">
              {post.laws[1].title}
            </h2>
            {@html post.laws[1].content}
          </div>
          <div class="mb-6 prose prose-lg text-color3 lg:max-w-none lg:mb-0">
            <h2
              class="py-3 font-semibold leading-6 tracking-wide uppercase sm:text-xl text-mcorange2">
              {post.laws[2].title}
            </h2>
            <p>
              {@html post.laws[2].content}
            </p>
          </div>
          <div class="prose prose-lg text-color3">
            <h2
              class="py-3 font-semibold leading-6 tracking-wide uppercase sm:text-xl text-mcorange2">
              {post.laws[3].title}
            </h2>
            {@html post.laws[3].content}
          </div>
        </div>
        <div
          class="text-base text-lg text-center max-w-prose lg:max-w-none text-mcblack">
          <p>{$_('rights.disclaimer')}</p>
        </div>
      </div>
    </div>
  </div>
</div>
