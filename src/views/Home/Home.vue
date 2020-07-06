<template>
  <div class="h-screen flex">
    <!-- <p-image :image="selfImage" /> -->
    <banner />
    <description />
    <navMenu />
  </div>
</template>

<script>
export default {
  components: {
    banner: () => import("../../components/banner/BannerBox"),
    description: () => import("../../components/desciption"),
    navMenu: () => import("../../components/navMenu/navigation")

    // "p-image": () => import("../../components/base/image")
  },
  data() {
    return {
      selfImage:
        "https://images.unsplash.com/photo-1558531304-a4773b7e3a9c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80"
    };
  }
};
</script>
