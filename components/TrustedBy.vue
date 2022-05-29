<template>
    <div>
        <Section-Header text="Trusted by"></Section-Header> 
        <div class="flex flex-col sm:flex-row justify-center items-center gap-16 pointer-events-none mb-48">
          <div v-for="logo in trustedBy" :key="logo.id" style="filter: grayscale(100%);">
              <img :src="logo.image" :alt="logo.title" class="h-12 w-auto">
          </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            trustedBy:[
              {
                title: "Acceleprise",
                image: "acceleprise-logo.png",
              },
              {
                title: "German Accelerator",
                image: "german-accelerator-logo.svg",
              },
              {
                title: "User Interviews",
                image: "/ui-banner-squoosh.webp",
              },
            ],
        }
    }
}
</script>