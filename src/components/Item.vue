<template>
  <div>
    <li>
      <label for="">
        <input type="checkbox" v-model="todo.finished" />
        <span>{{todo.title}}</span>
      </label>
      <button class="btn btn-waring" style="display:none;">删除</button>
    </li>
  </div>
</template>

<script>
export default {
  props: {
    todo: Object
  },
  data () {
    return {

    }
  },
  computed: {

  },
  created () {

  },
  mounted () {

  },
  watch: {

  },
  methods: {

  },
  components: {

  }
}
</script>

<style lang="scss" scoped>
li {
  width: 100%;
  height: 40px;
  line-height: 40px;
  text-align: left;
  border: 1px solid #ccc;
}

label {
  margin-right: 10px;
}

button {
  float: right;
  width: 60px;
  height: 30px;
  margin-top: 5px;
  margin-right: 10px;
  border: none;
}
</style>
