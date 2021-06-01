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
  }
};
</script>
