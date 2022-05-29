<template>
    <div>
        <Section-Header text="Featured in"></Section-Header>
        <Section-Subheader title=" UserInterviews.com:"></Section-Subheader> 
        <a v-for="press in press" :key="press.id" :href="press.url" target="_blank" class="bg-white rounded-md shadow-lg border border-gray-200 mb-32 cursor-pointer overflow-hidden grid sm:grid-cols-5 items-center hover:shadow-xl transition duration-150 hover:border-gray-300 mx-4">
        <div class="col-span-1 sm:col-span-3 font-publicSans p-4 sm:p-6 md:p-8 lg:px-12">
            <div class="text-xl tracking-wider font-semibold mb-3">{{press.title}}</div>
            <div class="text-lg text-gray-500">{{press.description}}</div>
        </div>
        <img class="col-span-1 sm:col-span-2 object-cover w-full h-64 sm:h-full pointer-events-none" :src="press.imageSource" :alt="press.title">
        </a>
    </div>
</template>

<script>
export default {
    data() {
        return {
            press: [
                {
                title: "How to Use Prototype Testing to Create Emotionally Satisfying User Experiences",
                url: "https://www.userinterviews.com/blog/prototype-testing-process",
                description: "User research through user testing has some important pitfalls that can send you headed in the wrong direction. Learn some of the most important things to watch out for.",
                imageSource: "/User-Interviews-squoosh.webp",
                },
            ],
        }
    }
}
</script>