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

  <section class="grid md:grid-cols-3 mt-8 gap-10">
    <Post :posts="posts" />
  </section>
</template>
