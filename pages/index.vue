<template>
  <div>
    <h2>Hello from the main page</h2>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias ullam
      consequuntur quaerat, est aperiam quis quos eos maiores? Repellat dolores
      dolor quasi corporis quidem iste aspernatur, perferendis reiciendis
      explicabo tempore.
    </p>
  </div>
</template>

<script setup>
useSeoMeta({
  title: "Main page",
  ogTitle: "Main Page",
  description: "This is the main nuxt page",
  ogDescription: "This is my amazing site, let me tell you all about it.",
  ogImage: "https://example.com/image.png",
  twitterCard: "summary_large_image",
});
</script>
