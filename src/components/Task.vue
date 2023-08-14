<template>
     <div @dblclick="$emit('toggle-reminder')" :class="[task.reminder ? 'reminder' : '','task']">
          <h3>
               {{ task.text }}
               <i @click="$emit('delete-task')" class="fas fa-times"></i>
          </h3>
          <p>{{ task.day }}</p>
     </div>
</template>

<script>
     export default {
          name: 'Task',
          props: {
               task: Object
          }
     }
</script>

<style scoped>
     .task {
          padding: 10px;
          margin: 5px 0;
          border-radius: 5px;
          background-color: rgb(234, 231, 231);
          cursor: pointer;
          user-select: none;
          transition: .3s;
          border-left: 0px solid greenyellow;
     }

     .task:hover {
          opacity: 0.8;
     }

     .task h3 {
          display: flex;
          font-size: 1.1rem;
          justify-content: space-between;
          padding-right: 10px;
     }

     .task p {
          font-size: 0.9rem;
     }

     .task.reminder {
          border-left: 5px solid greenyellow;
     }

     .fas {
          color: crimson;
          cursor: pointer;
     }
</style>