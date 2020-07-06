<template>
  <div id="app" :class="background">
    <router-view />
  </div>
</template>
<script>
export default {
  data() {
    return {
      background: "bg-dark-800 text-white h-screen overflow-hidden"
    };
  }
};
</script>