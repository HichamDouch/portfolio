<template>
  <nav class="flex items-center justify-end h-screen w-1/2">
    <ul class="flex flex-col items-center px-8 justify-center border border-red-600 leading-12">
      <li
        v-for="(link,index) in  menuItems"
        :key="index"
        :id="index"
        class="flex flex-row-reverse justify-center px-4 my-3 cursor-pointer bg-dark-600 hover:bg-purple-600 rounded-full w-full items-center"
        @mouseenter="selectItem(index)"
        @mouseleave="selectItem(-1)"
      >
        <i v-html="link.icon" class="py-4"></i>
        <p class="px-2" v-if="false">{{link.label}}</p>
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
      hoveredItem: -1,
      id: null
    };
  },
  computed: {
    menuItems: function() {
      return navMenu.map((item, index) => {
        console.log(index);
        return {
          label: item.title,
          icon: item.icon
        };
      });
    }
  },
  mounted() {
    this.menuItems;
  },
  methods: {
    selectItem: function(id) {
      this.hoveredItem = id;
    }
  }
};
</script>

<style lang="scss" scoped>
</style>