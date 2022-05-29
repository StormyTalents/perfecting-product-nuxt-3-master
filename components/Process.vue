<template>
    <div id="process">
        <Section-Header text="Our Process"></Section-Header> 
        <div v-for="process in process" :key="process.id" class="sm:flex bg-white rounded-md shadow-lg border border-gray-200 overflow-hidden m-4 mb-12 lg:mb-24">
            <div class="p-4 md:p-8 lg:p-12 sm:w-3/5">
                <div class="text-2xl sm:text-3xl lg:text-3xl tracking-wide font-semibold mb-2">
                    {{process.stage}}
                </div>
                <div class="text-lg lg:text-lg text-gray-500 font-publicSans tracking-wide font-light">
                    {{process.description}}
                </div>
            </div>
            <div class="sm:w-2/5 flex items-center" :class="process.backgroundColor">
                <img :src="process.image" :alt="process.stage" class="mx-auto h-64 object-contain p-8 lg:p-10 pointer-events-none">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            process: [
                {
                    stage: "User Interviews",
                    description: "We interview the people who use your product or the people who you would want to and uncover painpoints, motivations, and how these people intersect with your business and product.",
                    pattern: "topography",
                    backgroundColor: "bg-blue-400",
                    image: "blue-interview-group.png",
                  },
                  {
                    stage: "User Testing",
                    description: "We test your product and create full product teardowns with annotations of your product and direct competitors', identify issues in user experience, and find features users want.",
                    pattern: "tictactoe",
                    backgroundColor: "bg-red-400",
                    image: "/Annotated Screens.png",
                  },
                  {
                    stage: "Product Strategy",
                    description: "We use UX research to solve problems with product engagement, retention and monetization by identifying key points of user friction, existing and unsolved problems, and compelling new product features.",
                    pattern: "temple",
                    image: "product-market-fit.png",
                    backgroundColor: "bg-green-400",
                },
            ],
        }
    }
}
</script>