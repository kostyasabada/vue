<script>
  export default {
    data() {
      return {
        name: 'john doe',
        status: true,
        tasks: ['Task 1', 'Task 2', 'Task 3']
      };
    }
  };
</script>

<template>
  <h1>Hello, {{ name }}!</h1>
  <p v-if="status">Status: Active</p>
  <p v-else>Status: Inactive</p>

  <h3>Tasks</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
</template>
