<template>
  <button class="text-lg font-bold rounded-md hover:shadow-lg bg-indigo-500 hover:bg-indigo-400 text-indigo-50 hover:text-white tracking-wide transition duration-150 py-2 px-6">
    <a href="https://calendly.com/perfecting-product/intro-call">
      {{ text }}
    </a>
  </button>
</template>

<script>
export default {
    props: [
        "text",
    ]
}
</script>