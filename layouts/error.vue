<template>
  <div>
    <h1 v-if="error.statusCode">{{ error.message }}</h1>
    <h1 v-else>应用发送异常</h1>
    <button @click="$router.replace('/home')">跳转到首页</button>
  </div>
</template>

<script>
export default {
  // 接受错误信息 error: {statusCode,message}
  props: ["error"],
  mounted() {
    console.log("error", this.error);
  }
};
</script>
