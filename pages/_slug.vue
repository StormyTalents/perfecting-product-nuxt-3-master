<template>
  <div>
    <h1 class="text-center text-3xl lg:text-4xl text-gray-800 font-semibold mt-24 mb-12">
      {{ article.title }}
    </h1>
    <Nuxt-Content
      :document="article"
      class="font-publicSans prose lg:prose-xl max-w-screen-md px-4 sm:px-0 mx-auto my-16"
    ></Nuxt-Content>
    <GetStarted />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content("pages", params.slug).fetch();
    return { article };
  },
};
</script>