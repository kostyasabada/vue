<script>
  export default {
    data() {
      return {
        name: 'john doe',
        status: 'active',
        tasks: ['Task 1', 'Task 2', 'Task 3'],
        link: 'https://www.google.com'
      };
    },
    methods: {
      toggleStatus() {
        this.status = this.status === 'active' ? 'inactive' : 'active';
      }
    }
  };
</script>

<template>
  <h1>Hello, {{ name }}!</h1>
  <p v-if="status === 'active'">Status: Active</p>
  <p v-else>Status: Inactive</p>

  <h3>Tasks</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>
  <!-- <a v-bind:href="link" target="_blank">Visit Google</a> -->
   <a :href="link">Visit Google</a>

   <button v-on:click="toggleStatus">Change Status</button>
</template>
