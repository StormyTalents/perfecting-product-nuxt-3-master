<template>
  <div class="!max-w-none sm:flex flex-row-reverse items-center justify-between min-h-[600px] gap-6 mb-6">
    <div class="mb-6 md:mb-0 mt-12 md:mt-0 mx-4 pl-6 xl:pl-[2vw]">
      <div class="max-w-screen-md xl:max-w-[60vw] text-3xl md:text-3xl lg:text-5xl xl:text-[4vw] font-extrabold mb-4 md:mb-3">
        {{ heroSection.customerGoal }}
      </div>
      <div class="max-w-screen-sm xl:max-w-[50vw] text-xl xl:text-[2vw] xl:leading-tight font-light text-gray-500 mb-8">
        {{ heroSection.solutionStatement }}
      </div>
      <Button text="Get Started" />
    </div>
    <div class="">
     <img src="/ecommerce-mobile&desktop.png" alt="" class="pointer-events-none max-h-[480px] xl:max-h-[35vw] mx-auto">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      color: "bg-yellow-200",
      heroSection:{
        customerGoal: "Create better product experiences",
        problemStatement: "Fed up with having little to no product-led growth?",
        solutionStatement: "Make users happy with the experiences they like.",
      }
    }
  },
  methods: {
    toggleColor() {
      this.color = '!bg-red-200'
    },
  }
}
</script>
