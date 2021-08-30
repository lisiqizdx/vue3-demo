<template>
  <div class="hello">
    <h1>{{ newmsg }}</h1>
    <h2>{{accevalue}}</h2>
   <button @click="sonsendValue">sonSend</button>
  </div>
</template>

<script>
import{ ref } from 'vue'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  setup(props,context){
    const newmsg = ref(props.msg)
    const accevalue = ref('子组件默认值')
    const acceptvalue=(value)=>{
      accevalue.value = value
      newmsg.value = value
    }
    const sonsendValue=()=>{
      newmsg.value = props.msg
      accevalue.value = '子组件默认值'
      context.emit('my-son','子组件传值父组件')
    }
    return{
      newmsg,
      accevalue,
      acceptvalue,
      sonsendValue
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
