<script>
export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      name: 'jonn doe',
      status: 'pending',
      tasks: [
        'Task one',
        'Task two',
        'Task three'
      ],
      link: 'https://www.google.com'
    }
  },
  methods: {
    toggleStatus() {
      // this.status = 'active'
      if(this.status === 'active') {
        this.status = 'pending'
      } 
      else if(this.status === 'pending') {
        this.status = 'inactive'
      }
      else {
        this.status = 'active'
      }
    }
  }
}
</script>

<template>
  <h1>{{name }}</h1>
  <p v-if="status === 'active' ">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>

  <!-- <a v-bind:href="link">Google</a> -->
  <a :href="link">Googlee</a>
  <br/>
  <!-- <button v-on:click="toggleStatus">change status</button> -->
  <button @click="toggleStatus">change status</button>

</template>

<style scoped>
  h1 {
    color: red;
  }

</style>