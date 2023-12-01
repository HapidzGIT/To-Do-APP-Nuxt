<template>
  <main>
    <h1>Hari ini mau ngapain aja ?</h1>
    <h2>Manage waktumu dengan lebih baik </h2>
    
    <div class="create-new">
      <input 
        type="text" 
        v-model="newTask" 
        placeholder="Atur waktumu lebih baik" 
        @keypress.enter="addTask" />
      <button @click="addTask">Tambah</button>
    </div>

    <div class="tasks">
      <Task
        v-for="(task, i) in $store.state.tasks"
        :key="i"
        :task="task" />
    </div>
    <div class="isi">
      <svg class="img" width="340" height="340"  viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                    <path fill="#508D69" d="M31.2,-51.3C41.1,-42.2,50.2,-34.6,61.2,-24C72.2,-13.3,85.2,0.4,86.6,14.6C87.9,28.9,77.7,43.7,65.8,56.3C53.8,69,40.1,79.5,26.3,78.4C12.5,77.4,-1.3,64.6,-17,59.4C-32.7,54.2,-50.2,56.4,-57.6,49.2C-65,41.9,-62.3,25.3,-63,10C-63.7,-5.2,-67.7,-19,-65.9,-33.1C-64.1,-47.1,-56.4,-61.5,-44.5,-69.6C-32.5,-77.7,-16.3,-79.5,-2.8,-75.1C10.7,-70.8,21.3,-60.3,31.2,-51.3Z" transform="translate(100 100)" />
                  </svg>
    </div>
  </main>
</template>

<script>
export default {
  data (){
    return {
      newTask: ''
    }
  },
  methods: {
    addTask () {
      if (this.newTask) {
        this.$store.commit('ADD_TASK', this.newTask);
        this.newTask = '';
      }
    }
  }
}
</script>
