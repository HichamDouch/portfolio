<template>
  <div class="border-35 border-purple-600 border-r-0 rounded-tr-md bg-dark w-full p-12 relative">
    <div class="shadow-3xl w-full rounded-lg h-full absolute top-0 left-0 bg-no-repeat">
      <div
        class="w-full h-full bg-contain bg-no-repeat"
        :style="{backgroundImage: `url(${selfPic})`}"
      ></div>
      <!-- <div :style="{backgroundImage: `url(${selfPic})`}" class="bg-cover h-full bg-no-repeat"> -->
      <!-- <p
            class="bg-white text-gray-400 text-lg border border-white py-2 px-8 uppercase rounded"
      >looooool</p>-->
      <!-- </div> -->
    </div>
    <!-- <div class="h-screen bg-white w-1/2 absolute top--10"></div> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      selfPic: require("E:/Pictures/self/Photo.jpg")
      // selfPic:
      // "https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80"
    };
  }
};
</script>

<style></style>
