<template>
  <div class="goods">
    <h2>goods</h2>
    <nuxt-link to="/goods/1?a=1&b=2">goods No.1</nuxt-link>
    <nuxt-link to="/goods/2?a=11&b=22">goods No.2</nuxt-link>
    <nuxt-link :to="{name:'goods-id',params:{id:3},query:{a:111,b:222}}">goods No.3</nuxt-link>
    <nuxt-link to="/goods/comment">goods comment</nuxt-link>

    <Nuxt />
  </div>
</template>
