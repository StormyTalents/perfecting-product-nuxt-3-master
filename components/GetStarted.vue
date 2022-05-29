<template>
    <div class="mt-16 md:mt-32 mb-32 md:mb-48 md:grid gap-4 md:grid-cols-4 lg:grid-cols-5 justify-center mx-4">
      <div class="md:col-span-2 lg:col-span-3 text-2xl md:text-3xl lg:text-5xl font-medium md:leading-snug px-4 py-12 md:py-24">
        Get started creating product-led growth
      </div>
      <form name="contact" action="POST" data-netlify="true" data-netlify-honeypot="bot-field" class="col-span-2 flex flex-col gap-6 bg-gradient-to-br from-gray-100 to-gray-50 rounded-xl border shadow-xl hover:shadow-2xl transition duration-300 py-12 md:py-24 px-12 text-lg">
        <input type="hidden" value="contact" name="form-name" />
        <label>Your First Name: <input type="text" name="name" required="true" class="w-full rounded border shadow focus:outline-none px-6 py-4"/></label>
        <label>Your Business Email: <input type="email" name="email" required="true" class="w-full rounded border shadow focus:outline-none px-6 py-4"/></label>
        <button type="submit" class="bg-black text-gray-100 hover:text-white py-4 px-6 rounded-md hover:bg-gray-800 hover:shadow-lg transition duration-150">Submit</button>
      </form>
    </div>
</template>