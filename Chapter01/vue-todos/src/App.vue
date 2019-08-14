<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="todo in todos">
        <label>{{ todo.value }}</label>
      </li>
    </ul>
    <hr>
    <ul>
      <li v-for="(todo,index) in todos"
          :id="index">
        <label>{{ index + 1 }}.{{ todo.value }}</label>
      </li>
    </ul>
    <hr>
    <!-- v-for不单单可以循环渲染数组，还可以渲染对象属性，例如：-->
    <ul>
      <li v-for="value in object">
        {{ value }}
      </li>
    </ul>
  </div>
</template>

<style></style>

<script>
  export default {
    name: 'app',
    data () {
      return {
        title: "vue-todos",
        todos: [
          { value: "阅读一本关于前端开发的书", done: false },
          { value: "补充范例代码", done: true },
          { value: "写心得", done: false }
        ],
        object: {
          first_name : "Ray",
          last_name : "Liang"
        }
      }
    }
  }
</script>
