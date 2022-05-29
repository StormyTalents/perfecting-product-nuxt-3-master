<template>
  <div class="font-publicSans px-4">
    <h1 class="text-center text-3xl tracking-wide font-publicSans font-bold mt-8 md:mt-16 mb-6">
        UX Research Case Studies
    </h1>
    <ul class="grid md:grid-cols-2 gap-4 mb-12 md:mb-24">
      <li v-for="article of articles" :key="article.slug" class="bg-white rounded-md shadow hover:shadow-lg transition duration-150 border overflow-hidden">
        <NuxtLink :to="'/case-studies/'+article.slug" class=" cursor-pointer">
          <img :src="article.img" class="max-h-96 pointer-events-none" />
          <div class="p-4">
            <p class="text-xs text-blue-500 uppercase font-bold">{{article.tag}}</p>  
            <h2 class="text-2xl font-bold text-gray-800 tracking-wide leading-tight mb-1">{{ article.title }}</h2>
            <p class="text-base text-gray-500 tracking-wide">{{ article.description }}</p>
          </div>
        </NuxtLink>
      </li>
    </ul>
    <Subscribe />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const articles = await $content("case-studies")
      .sortBy("date", "desc")
      .fetch();
    return {
      articles,
    };
  },
  head() {
      return {
          title: this.articles.slug,
      }
  }
};
</script>