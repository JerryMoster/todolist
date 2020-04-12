<template>
  <div class="todo-contaiiner">
    <div class="todo-wrap">

      <Head />
      <List :todoL="todos" />
      <Foot />
    </div>
  </div>
</template>

<script>
import Head from './components/Head.vue'
import List from './components/List.vue'
import Foot from './components/Foot.vue'

export default {
  name: 'App',
  data () {
    return {
      todos: [
        { title: '中国北京', finished: false },
        { title: '中国上海', finished: false },
        { title: '中国广州', finished: false },
        { title: '中国深圳', finished: false }
      ]
    }
  },
  components: {
    Head,
    List,
    Foot
  }
}
</script>

<style scoped>
</style>
