<template>
  <div id="app">
    <div class="container">
      <div class="row header mb-5 p-3">
        <div class="col-lg-12">
          <h2>What I do Today?</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-lg-12">
          <div class="home-work">
            <div class="row">  
              <div v-for="taskMe in tasks" v-bind:key="taskMe.id" class="mb-3 tasks col-lg-12 text-left">
                <div class="form-check">
                  <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
                  <label class="form-check-label item" v-bind:class="{'item-done':taskMe.status}" for="defaultCheck1">
                    {{ taskMe.nameTask }}
                  </label>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'

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
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.header{
  background: #3057da;
  color: #ffffff;
}

.header h2{
  margin: 0;
}

.tasks .item{
  font-size: 20px;
}

.item-done{
  color: #b8b8b8;
}
</style>
