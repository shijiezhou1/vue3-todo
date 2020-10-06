<template>
  <ul>
    <li
      v-for="(todolist, index) in TodoLists"
      :key="index"
    >
      <span class="name">{{todolist.name}}</span>
      <span
        class="delete"
        @click="Delete(todolist.id)"
      >x</span>
    </li>
  </ul>
</template>

<script>

export default {
  props: {
    TodoLists: Array,
    Delete: Function
  },
}
</script>

<style scope>
ul {
  list-style: none;
  flex-direction: column;
  width: 50%;
  margin: auto;
}

li {
 display: flex;
margin:5px 0;
justify-content: space-between;
align-content: center;
}

.name {
  font-weight: bold;
}

.delete {
  background-color: red;
  color: white;
  padding: 0 10px;
  line-height: 1;
  border-radius: 5px;
}
</style>