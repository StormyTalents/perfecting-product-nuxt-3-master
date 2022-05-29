<template>
    <div class="bg-white border shadow sticky top-0 z-10">
      <nav class="flex justify-between items-center max-w-screen-lg p-4 mx-auto font-medium">
        <NuxtLink class="text-xl font-medium" to="/">Perfecting Product</NuxtLink>
        <div class="flex gap-4">
          <NuxtLink v-for="nav in nav" :key="nav.id" class="block rounded-sm py-2 px-3 hover:bg-gray-200" :to="nav.link">{{nav.title}}</NuxtLink>
          <NuxtLink class="bg-yellow-400 hover:bg-yellow-300 text-black hover:text-gray-900 py-2 px-4 rounded hover:shadow-lg transition duration-150" to="/contact">Work With Us</NuxtLink>
        </div>
      </nav>
    </div>
</template>

<script>
export default {
  data() {
    return {
      nav: [
        {
          link: "/services",
          title: "Services"
        },
        {
          link: "/case-studies",
          title: "Case Studies"
        },
        {
          link: "/blog",
          title: "Resources"
        },
        {
          link: "/about",
          title: "About"
        },
      ]
    }
  }
}
</script>