<template>
  <div>
    <article class="max-w-screen-md py-8 mx-auto mb-12">
      <p class="text-xs md:text-sm text-blue-500 font-bold uppercase px-4 sm:px-0 mb-1">
        {{ article.tag }}
      </p>
      <h1 class="text-xl md:text-4xl text-gray-800 font-bold px-4 sm:px-0 mb-1">{{ article.title }}</h1>
      <p class="text-base md:text-xl text-gray-500 px-4 sm:px-0 mb-3">{{ article.description }}</p>
      <img :src="article.img" :alt="article.alt" class="mb-3"/>
      <Nuxt-Content
        :document="article"
        class="prose lg:prose-xl font-publicSans px-4 sm:px-0"
      ></Nuxt-Content>
    </article>
    <GetStarted />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content("articles", params.slug).fetch();

    return { article };
  },
  head() {
    return {
      title: this.article.title + " | Perfecting Product",
      meta: [
        { hid: 'og:title', name: 'og:title', content: this.article.title + ' | Perfecting Product' },
        { hid: 'og:image', property:"og:image", content:"https://www.perfectingproduct.com/" + this.article.img },
        { hid: 'og:description', property:"og:description", content: this.article.description },
      ],
    } 
  }
};
</script>