<template>
  <div id="app">
    <div class="container">
      <div class="row header">
        <h2 class="col-lg-12">What I do Today?</h2>
      </div>
    </div>

    <div class="container">
      <div class="row content">
        <div class="col-lg-12">
          <div class="home-work">
            <div v-for="taskMe in tasks" v-bind:key="taskMe.id" class="tasks">
              <p>{{ taskMe.nameTask }}</p>
            </div>
          </div>
        </div>
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
          nameTask: 'Washing clothes',
          status: false
        },
        {
          id: 2,
          nameTask: 'Learning online course',
          status: false
        },
        {
          id: 3,
          nameTask: 'Repairing motorcycle',
          status: false
        },
        {
          id: 4,
          nameTask: 'Creating study case',
          status: false
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
