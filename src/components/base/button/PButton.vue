<template>
  <button
    @mouseenter="mouseEnter"
    @mouseleave="mouseLeave"
    class="transition duration-300 ease bg-yellow py-2 w-2/6 rounded-full focus:outline-none flex justify-center items-center"
  >
    <p>{{text}}</p>
    <slot></slot>
    <transition name="icon-fade">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        v-show="active"
        height="22"
        color="red"
        viewBox="0 0 24 24"
        width="24"
        class="mx-1"
      >
        <path d="M0 0h24v24H0z" fill="none" />
        <path
          fill="white"
          d="M12 12c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"
        />
      </svg>
    </transition>
  </button>
</template>

<script>
export default {
  props: {
    text: {
      type: String
    },
    variant: {
      type: String
    },
    form: {
      type: String,
      default: "cercle"
    }
  },
  data() {
    return {
      active: false
    };
  },
  methods: {
    mouseEnter: function() {
      this.active = !this.active;
    },
    mouseLeave: function() {
      this.active = !this.active;
    }
  }
};
</script>

<style  scoped>
.icon-fade-enter-active,
.icon-fade-leave-active,
.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease;
}

.icon-fade-enter,
.icon-fade-leave-to {
  transform: translateX(-20px);
  opacity: 0;
}
.icon-fade-enter-to,
.icon-fade-leave {
  transform: translateX(0px);
  opacity: 1;
}
</style>