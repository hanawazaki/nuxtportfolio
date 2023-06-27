<template>
  <section>
    <h1 class="text-5xl font-bold mt-20">Hello, I'm Hairul Ardhan Nawazaki!</h1>
    <p class="text-base text-gray-900 p-2 italic">Frontend web Developer</p>
  </section>
  <section class="flex flex-col md:flex-row">
    <div class="md:w-3/4">
      <h2 class="text-3xl font-bold mt-8">My Story</h2>
      <p class="text-lg py-2">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ab, architecto
        laboriosam dignissimos perferendis illum debitis porro nostrum sed,
        consectetur dolorum, pariatur obcaecati. Laudantium sit veniam, optio
        molestiae vitae ducimus voluptate et hic rerum. Explicabo quis quae
        pariatur autem? Nostrum, reiciendis dolores molestias neque similique
        fugit incidunt deleniti quo natus est.
      </p>
      <p class="text-lg py-2">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorum amet
        ratione fuga natus maxime reiciendis cumque ducimus vero officia
        asperiores excepturi, quisquam provident nam dolorem eveniet similique
        reprehenderit sequi. Modi et rem nobis iste dignissimos, veniam
        asperiores id nisi soluta unde illum aliquid reprehenderit laborum
        neque? Assumenda itaque accusantium quos?
      </p>
    </div>
    <img
      src="../assets/images/person.png"
      alt=""
      class="w-1/2 md:max-w-sm p-8 mx-auto"
    />
  </section>
  <section>
    <h2 class="text-3xl font-bold mt-8">Latest Blog Posts</h2>
    <div class="grid grid-cols-3 pt-8 gap-10">
      <Post :posts="posts" />
    </div>
  </section>
</template>

<script setup>
const { data: posts } = await useAsyncData("latest-posts", () =>
  queryContent("/blog").sort({ data: 1 }).limit(3).find()
);
</script>

<style lang="scss" scoped></style>
