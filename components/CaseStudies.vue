<template>
    <div class="flex flex-col justify-center">
        <Section-Header text="Read the Case Study"></Section-Header>
        <a href="/case-studies/terrific-tasks-case-study" class="md:mx-auto md:flex rounded-2xl shadow-xl shadow-indigo-100 overflow-hidden border mx-4 hover:scale-105 duration-200">
            <div class="bg-white p-4 md:p-10">
                <p class="text-xs text-indigo-500 uppercase font-bold">case study</p>
                <h2 class="text-3xl font-bold text-gray-800 tracking-wide leading-tight mb-1">Drive Product-Led Growth by Identifying Compelling New Product Features</h2>
                <p class="text-lg text-gray-400 font-light tracking-wide leading-snug">Unsolved user problems drive users to switch to new products. You can identify compelling user problems and solutions that you can craft into product features that people are willing to pay for.</p>
            </div>
            <div class="flex items-center justify-center bg-gradient-to-br from-[#fb923c] to-[#fb7185] via-red-400 p-24">
                <div class="text-6xl font-extrabold drop-shadow-lg text-red-50">
                Terrific Tasks
                </div>
            </div>
        </a>
    </div>
</template>

<script>
export default {
    data() {
        return {
            links: [
                {
                    link:"/case-studies/terrific-tasks-case-study",
                    image:"/terrific-tasks.png",
                    alt:"",
                },
                // {
                //     link:"/case-studies/terrific-tasks-case-study",
                //     image:"/if-you-bought-crypto-when.png",
                //     alt:"",
                // },
            ]
        }
    }
}
</script>