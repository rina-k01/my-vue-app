<template>
  <div class="todolist">
    <div>Todoリスト</div>
    <div>
      <div v-for="(todo, index) in todos" v-bind:key="index" class="todo">
        <div class="todo__checkbox">
          <input type="checkbox" v-model="todo.isDone" />
        </div>
        <div v-if="todo.isDone" class="todo__text todo__text--done">
          {{ index }}:{{ todo.text }}
        </div>
        <div v-else class="todo__text">{{ index }}:{{ todo.text }}</div>
        <div v-on:click="deleteTodo(index)" class="todo__delete">削除</div>
      </div>
    </div>
    <div>
      <div>
        <input type="text" v-model="inputTodo" />
        <div v-on:click="addTodo">追加</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputTodo: "",
      todos: [
        {
          text: "ひき肉を300g買う",
          isDone: false,
        },
        {
          text: "ホウレンソウを1束買う",
          isDone: false,
        },
        {
          text: "ピーマンを2個買う",
          isDone: false,
        },
      ],
    }
  },
  methods: {
    addTodo() {
      if (this.inputTodo !== "") {
        const todo = { text: this.inputTodo, isDone: false }
        this.todos.push(todo)
      }
    },
    deleteTodo(index) {
      this.todos.splice(index, 1)
    },
  },
}
</script>

<style scoped>
.todolist {
  padding-left: 5rem;
  padding-right: 5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.todo {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem;
  border-radius: 5px;
}

.todo:hover {
  color: white;
  background-color: #b23b61;
}

.todo__text {
  margin-left: 2rem;
  text-align: left;
}

.todo__text--done {
  text-decoration-line: line-through;
}

.todo__delete {
  margin-left: 2rem;
  padding: 0.5rem 0.5rem;
}

.todo__delete:hover {
  margin-left: 2rem;
  background-color: #b2ae3b;
  border-radius: 5px;
}
</style>
