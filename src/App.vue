<template>
  <div id="nav">
    {{msg}}
  </div>
</template>

<script lang="ts">
import {ref} from 'vue'
export default {
  //新的API,可以将vue2中的data,methods,computed,watch以及生命周期函数写在里面。
  //该方法的返回值如果返回的是一个对象,那么对象中的属性就会被暴露到模板中,可以在HTML模板中直接使用
  //该方法的执行时机比生命周期函数created还要早,也就是说该方法执行时还没有创建实例对象,this的值是undefined
  setup(){
    const msg = ref('hello vue3')
    return {
      msg
    }
  }
}
</script>

