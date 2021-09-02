<template>
  <div class="home">
   <button @click="sendValue">send</button>
   <h1>{{sonmsg}}</h1>
    <HelloWorld ref="hello" @my-son='parantAccept' msg="父组件传值给子组件"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import{ ref } from 'vue'
export default {
  name: 'admin',
  components: {
    HelloWorld
  },
  setup(){
    const hello = ref();
    const sonmsg = ref('父组件接收值');
    const sendValue=()=>{
      sonmsg.value = '父组件接收值'
      hello.value.acceptvalue('父组件调用')
    }
    const parantAccept=(value)=>{
      sonmsg.value = value
    }
    return{
      hello,
      sonmsg,
      sendValue,
      parantAccept,
    }
  }
}
</script>
<style lang='scss'>
#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
