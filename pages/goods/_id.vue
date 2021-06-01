<template>
  <div class="details">
    goods details
  </div>
</template>
<script>
export default {
  name: "goods-detail",
  validate({ params, query }) {
    return typeof params.id === "number";
  },
  transition:'test'
};
</script>

<style scoped>
/* .test-enter-active, .test-leave-active {
  transition: all ease 0.5;
}
.test-enter, .test-leave-to{
  margin-left: -1000px;
} */
</style>
