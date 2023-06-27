<script setup>
const { data: posts } = await useAsyncData("posts", () =>
  queryContent("/blog").find()
);
</script>
<template>
  <h1 class="text-3xl my-8">Blog Posts</h1>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem
  necessitatibus, doloremque odit, animi aut repellat explicabo dolorem culpa
  nam, repudiandae consequuntur dolorum similique. Molestias in tenetur
  obcaecati ipsum, minima quasi non minus quo laudantium soluta sapiente modi,
  dicta sint iste recusandae explicabo maxime facere ducimus ex quia! Ipsum, non
  modi!

  <ul>
    <li v-for="post in posts" :key="post._id" class="my-8 py-4 border-b-2">
      <nuxt-link :to="post._path" class="text-blue-500 text-2xl">{{
        post.title
      }}</nuxt-link>
      <p class="text-gray-500">{{ post.description }}</p>
    </li>
  </ul>
</template>
