<template>
  <div id="hide-scroll-content" class="square">
    <div class="child">child 1</div>
    <div class="child">child 2</div>
    <div class="child">child 3</div>
  </div>
</template>

<script>

export default {
  mounted() {
      this.openLoading();
  },
  components: {},
  methods: {
    openLoading() {
      const loading = this.$vs.loading({
        type : "corners"
      });
      this.hasOpenLoading = true;
      setTimeout(() => {
        loading.close();
      }, 3000);
    },
  },
};
</script>

<style></style>
