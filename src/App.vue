<template>
  <div id="app">
    <h2>What I do Today?</h2>
    <div class="home-work">

      <div v-for="taskMe in tasks" v-bind:key="taskMe.id" class="tasks">
        <p>{{ taskMe.nameTask }}</p>
      </div>

    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: function(){
    return{
      tasks: [
        {
          id: 1,
          nameTask: 'Washing clothes'
        },
        {
          id: 2,
          nameTask: 'Learning online course'
        },
        {
          id: 3,
          nameTask: 'Repairing motorcycle'
        },
        {
          id: 4,
          nameTask: 'Creating study case'
        },
      ]
    };
  },
  components: {
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
