<template>
  <div id="expert">
    <Section-Header text="Who you'll be working with:"></Section-Header> 
    <div class="flex flex-col gap-16 md:flex-row items-start justify-between text-base tracking-wider px-0 py-0 m-4">
        <div class="border-4 border-indigo-200 rounded-tl-[20%] rounded-tr-[16%] rounded-bl-[16%] rounded-br-[65%] overflow-hidden shadow-xl shadow-indigo-200">
          <img class="h-full mx-auto pointer-events-none" src="/headshot_squoosh.jpeg" alt="Christian von Uffel">
        </div>
        <div class="bg-white rounded-lg border border-slate-200 shadow-lg p-4 px-6 md:py-8 md:px-12">
          <div class="mb-3">
            <div class="text-2xl font-bold text-indigo-500">
              UX Research Manager &#38; Product Leader
            </div>
            <div class="text-xl text-gray-500 font-medium">
              Christian von Uffel
            </div>
          </div>
          <ol class="text-gray-700 text-base lg:text-lg font-medium leading-relaxed list-disc pl-4">
            <li v-for="bullet in bulletPoints" :key="bullet.id" class="mb-1">{{bullet}}</li>
          </ol>
        </div>
      </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            bulletPoints:[
              "led UX research for a crypto finance platform with over a million users",
              "launched two 6-figure award-winning products",
              "SaaS product & marketing mentor for 5+ years",
              "surveyed 20k+ users",
              "interviewed 250+ users",
              "managed 500+ user tests",
            ],
        }
    }
}
</script>