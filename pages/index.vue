<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        nuxt-analyse1
      </h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {


  // middleware:'auth', // 页面层级中间件定义
  middleware(context){
    console.log('middleware pages')
  },

  //参数的有效性
  validate({params,query}){
    //校验业务
    console.log('validate')
    return true
  },

  //读取数据，返回给组件
  asyncData(context){
    //异步业务逻辑读取服务端数据
    console.log('asyncData')
    return {
      b:2
    }
  },

  //读取数据，vuex
  fetch({store}){
    //异步业务逻辑数据，读取服务端数据交给vuex
    console.log('fetch')
  },

  //SSR && CSR

  beforeCreate(){
    console.log('beforeCreate')
  },

  created(){
    console.log('created')
  },

  //CSR
  beforeMount(){
    console.log('beforeMount')
  },
  mounted(){
    console.log('mounted')
  },
  beforeUpdate(){
    console.log('beforeUpdate')
  },
  updated(){
    console.log('updated')
  },
  beforeDestroy(){
    console.log('beforeDestroy')
  },
  destroyed(){
    console.log('destroyed')
  },

  //服务端渲染 激活 失活 不存在
  // activated(){},
  // deactivated(){},

  data(){
    return {
      a:1
    }
  },

}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
