<template>
    <div>
        <!-- section header -->
        <SectionHeader text="Testimonials" />

        <!-- testimonial card -->
        <div v-for="testimonial in testimonials" :key="testimonial.id" class="md:flex items-start justify-between gap-16 rounded-lg shadow-lg border border-slate-200 font-publicSans p-6 py-8 md:px-12 lg:px-16 m-4 mb-16">
            <div class="flex flex-col">
                <div class="text-8xl font-italic text-indigo-400 opacity-50 h-20">
                    &ldquo;
                </div>
                <div class="text-lg md:text-xl font-regular text-[#64748b] tracking-wide md:leading-relaxed mb-8 sm:mb-0">
                    {{testimonial.content}}
                </div>
            </div>
            <div class="">
                <div class="rounded-tl-[20%] rounded-tr-[25%] rounded-bl-[65%] rounded-br-[36%] shadow-md shadow-indigo-100 w-52 border-4 border-indigo-200 overflow-hidden mx-auto mb-2 pointer-events-none">
                    <img :src="testimonial.imageSource" alt="testimonial.name">
                </div>
                <div class="text-center tracking-wide">
                    <div class="md:text-lg text-indigo-400 font-bold">{{testimonial.name}}</div>
                    <div class="text-[#52525b]">{{testimonial.title}}, {{testimonial.company}}</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            testimonials: [
                {
                name: "Mark Fershteyn",
                company: "Recapped.io",
                title: "Founder",
                content: "Christian has a rare ability to quickly identify problems in user experience and product. He immediately identified problems in our product’s onboarding process that we needed to solve, the next steps to fix them, and exactly how to measure the result of these changes.",
                imageSource: "/mark_squoosh.webp",
                },
                {
                name: "Alex Krupp",
                company: "FWD:Everyone",
                title: "Founder",
                content: "Christian helped us with user testing; he immediately identified a bunch of problems with our product and onboarding flow, and came up with pragmatic and easy-to-implement ways to improve our funnel.",
                imageSource: "Alex-Krupp.jpeg",
                },
                {
                name: "Ivan Homola",
                company: "Lunadio",
                title: "Founder",
                content: "I'm amazed by Christian's ability across multiple fields. From design to development to marketing. He always asks the right questions to figure out our issues in product positioning and user experience.",
                imageSource: "ivan.jpeg",
                },
            ],
        }
    }
}
</script>