<template>
  <div class="comment">
    <h3>comment</h3>
    <nuxt-link :to="{name:'goods-comment-uid',params:{uid:1},query:{a:1,b:2}}">comment No.1</nuxt-link>
    <nuxt-link to="/goods/comment/2?a=11&b=22">comment No.2</nuxt-link>
    <Nuxt />
  </div>
</template>
