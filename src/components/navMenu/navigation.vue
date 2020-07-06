<template>
  <nav class="flex items-center justify-end h-screen w-1/2">
    <ul class="flex flex-col items-center px-8 justify-center border border-red-600 leading-12">
      <li
        v-for="(link,index) in navMenu"
        :key="index"
        :id="index"
        class="flex flex-row-reverse justify-center px-4 my-3 cursor-pointer bg-dark-600 hover:bg-purple-600 rounded-full w-full items-center"
        @mouseenter="mouseEnter(index)"
        @mouseleave="mouseLeave(index)"
      >
        <i v-html="link.icon" class="py-4"></i>
        <p class="px-2" v-if="false">{{link.title}}</p>
      </li>
    </ul>
  </nav>
</template>

<script>
import navMenu from "./nav";
export default {
  data() {
    return {
      navMenu: navMenu,
      active: false,
      id: null
    };
  },
  methods: {
    mouseLeave: function() {
      this.id = null;
      console.log(this.id);
    },
    mouseEnter: function() {
      // if ((index === index, event.target.id)) {
      //   console.log(index, event.target.id);
      //   // this.active = !this.active;
      // }
      this.id = event.target.id;
      // console.log(this.id);
    }
  }
};
</script>

<style lang="scss" scoped>
</style>