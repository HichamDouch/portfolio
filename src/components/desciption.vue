<template>
  <div class="border border-red-800 h-screen flex pl-32">
    <div class="border flex flex-col justify-center p-2 leading-loose">
      <h4 class="text-xl font-light">HI THERE</h4>
      <h1 class="text-5xl font-bold">
        I'M
        <span class="font-bold text-purple-600">{{info.name}}</span>
      </h1>
      <p class="font-light text-lg">{{info.resume}}</p>
      <br />

      <pbutton text="MORE ABOUT ME"></pbutton>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      info: {
        name: "HICHAM DOUCH",
        resume:
          "I'm a Tunisian based web designer & front‑end developer focused on crafting clean & user‑friendly experiences, I am passionate about building excellent software that improves the lives of those around me."
      }
    };
  },
  components: {
    pbutton: () => import("../components/base/button/PButton")
  }
};
</script>
