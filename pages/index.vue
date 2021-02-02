<template>
<div class="square" id="hide-scroll-content">
  <div class="child">child 1</div>
  <div class="child">child 2</div>
  <div class="child">child 3</div>
</div></template>

<script>
export default {
  data() {
    return {
      hasOpenLoading: false,
      loading_types: [
        "default",
        "waves",
        "corners",
        "border",
        "points",
        "square",
        "gradient",
        "rectangle",
        "circles",
        "square-rotate",
        "scale",
      ],
      color : '#ff6600',
    };
  },
  mounted() {
    //call the loading when the component launch
    this.openLoading();
  },
  components: {},
  methods: {
    openLoading() {
      //create the oading
      const loading = this.$vs.loading({
        type: this.loading_types[8],
         color: this.color
      });

      //close the loading
      this.hasOpenLoading = true;
      setTimeout(() => {
        loading.close();
      }, 3000);
    },
  },
};
</script>

<style></style>
