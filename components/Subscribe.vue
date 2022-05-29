<template>
    <div id="subscribe" class="flex flex-col rounded-xl shadow-xl hover:shadow-2xl transition duration-300 bg-yellow-300 text-gray-900 px-10 md:px-12 py-12 md:py-16 mb-24 mx-4">
      <div class="text-3xl md:text-4xl font-semibold tracking-tighter">Subscribe to Perfecting Product</div>
      <form name="subscribe" action="post" data-netlify="true" class="mt-6 flex flex-col gap-4 md:inline-block">
        <input type="email" name="email" required="true" placeholder="enter your email" class="rounded-lg md:rounded-l-lg shadow text-lg border focus:outline-none  px-6 py-4">
        <button type="submit" class="shadow-lg bg-gray-800 hover:bg-gray-700 transition duration-150 text-lg text-white rounded-lg md:rounded-r-lg focus:outline-none px-6 py-4">Subscribe</button>
      </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            
        }
    }
}
</script>