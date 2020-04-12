<template>
  <div class="todo-contaiiner">
    <div class="todo-wrap">

      <Head :addTodo="addTodo" />
      <List :todoL="todos" :deleteTodo="deleteTodo" />
      <Foot :todosfoot="todos" :selectedAll="selectedAll" :deltetAll="deltetAll" />
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
        { title: '中国北京', finished: true },
        { title: '中国上海', finished: true },
        { title: '中国广州', finished: false },
        { title: '中国深圳', finished: false }
      ]
    }
  },
  components: {
    Head,
    List,
    Foot
  },
  methods: {
    // 根据索引删除这条纪律
    deleteTodo (index) {
      this.todos.splice(index, 1)
    },
    // 插入一条新的数据
    addTodo (todo) {
      this.todos.unshift(todo)
    },
    selectedAll (isCheck) {
      this.todos.forEach(function (todo) {
        todo.finished = isCheck
      })
    },
    // 删除选中的项目
    deltetAll () {
      this.todos = this.todos.filter(todo => !todo.finished)
    }
  }
}
</script>

<style scoped>
</style>
