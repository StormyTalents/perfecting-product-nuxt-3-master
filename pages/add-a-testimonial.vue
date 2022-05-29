<template>
  <div class="max-w-screen-md mx-auto">
    <!-- header -->
    <div class="text-center text-2xl md:text-3xl font-semibold m-10 mt-20">
      Add Your Own Customer Testimonial
    </div>
    <div class="text-center">this preview is responsive</div>

    <!-- testimonial card -->
    <div
      class="p-6 m-4 mb-8 shadow-lg border-solid border-gray-300 border rounded-md text-base sm:flex items-center"
    >
      <div class="text-center font-medium px-8 sm:w-2/5">
        <div class="rounded-full w-32 h-32 overflow-hidden mx-auto mb-2">
          <img v-bind:src="imageSource" :alt="name" />
        </div>
        <div>{{ name }}</div>
        <div>{{ title }}</div>
      </div>
      <div class="mt-2 md:mt-8 md:m-6">{{ testimonial }}</div>
    </div>

    <form
      name="testimonial"
      action="POST"
      data-netlify="true"
      data-netlify-honeypot="bot-field"
    >
      <div
        class="grid grid-cols-3 md:grid-cols-6 gap-6 font-medium items-center mx-2"
      >
        <input type="hidden" value="testimonial" name="form-name" />
        <label for="name">Name</label>
        <input
          v-model="name"
          name="name"
          class="col-span-2 border px-2 py-1 rounded"
          type="text"
          placeholder="Patrick Collison"
        />
        <label for="title">Title</label>
        <input
          v-model="title"
          name="title"
          class="col-span-2 border px-2 py-1 rounded"
          type="text"
          placeholder="CEO, Stripe"
        />
        <label class="testimonial" for="">Testimonial</label>
        <input
          v-model="testimonial"
          name="testimonial"
          class="col-span-5 border px-2 py-1 rounded"
          type="text"
          placeholder="What problem did we solve for you and how did we help?"
        />
        <label for="headshot">Headshot</label>
        <input
          v-model="imageSource"
          name="image_address"
          class="col-span-5 border px-2 py-1 rounded"
          type="url"
          id=""
          placeholder="Headshot image address (LinkedIn, Twitter, etc) at least 128px"
        />
      </div>
      <div class="flex justify-center mb-24">
        <button
          class="bg-yellow-400 hover:bg-yellow-300 text-black hover:text-gray-900 py-2 px-4 rounded hover:bg-gray-800 hover:shadow-lg transition duration-150 mt-6"
        >
          Submit Testimonial
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      title: "",
      testimonial: "",
      imageSource: "",
    };
  },
};
</script>