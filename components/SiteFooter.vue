<template>
  <footer class="bg-gray-800">
    <section
      class="mx-auto max-w-7xl px-2 sm:px-4 lg:py-6 text-gray-300 flex flex-row"
    >
      <p class="flex-1">
        &copy; Hairul Ardhan Nawazaki 2023. All Rights Reserved
      </p>
      <div class="flex flex-row justify-center gap-4 mb-4 mt-2">
        <a :href="link.href" v-for="link in links" :key="link.name">
          <Icon :name="link.icon" size="1.5rem" class="text-gray-300" />
        </a>
      </div>
    </section>
  </footer>
</template>

<script setup>
const links = [
  {
    name: "Github",
    href: "https://github.com",
    icon: "entypo-social:github-with-circle",
  },
  {
    name: "Twitter",
    href: "https://twitter.com",
    icon: "entypo-social:twitter",
  },
  {
    name: "Facebook",
    href: "https://facebook.com",
    icon: "entypo-social:facebook",
  },
  {
    name: "Linkedin",
    href: "https://linkedin.com",
    icon: "entypo-social:linkedin-with-circle",
  },
  {
    name: "Instagram",
    href: "https://instagram.com",
    icon: "entypo-social:instagram-with-circle",
  },
];
</script>

<style lang="scss" scoped></style>
