<template>
     <Header version="1.0"></Header>
     <Tasks :tasks="tasks"/>
</template>

<script>
     import Header from './components/Header.vue'
     import Tasks from './components/Tasks.vue'

     export default {
          name: 'App',
          components: {Header, Tasks},
          data() {
               return {
                    tasks: []
               }
          },
          created() {
               this.tasks = [
               {
                         id: 1,
                         text: "Doctor's Appointment",
                         day: 'January 1st at 12:00am',
                         reminder: true
                    },
                    {
                         id: 2,
                         text: "Meeting at School",
                         day: 'January 1st at 13:00am',
                         reminder: true
                    },
                    {
                         id: 3,
                         text: "Food shopping",
                         day: 'January 1st at 16:00am',
                         reminder: false
                    }
               ]
          }
     }
</script>

<style>
     * {
          margin: 0;
          border: 0;
          padding: 0;
          box-sizing: border-box;
     }

     #app {
          font-family: Avenir, Helvetica, Arial, sans-serif;
          -webkit-font-smoothing: antialiased;
          -moz-osx-font-smoothing: grayscale;

          margin: 0 auto;
          width: 50%;
          border: 1px solid black;
          border-radius: 10px;
          padding: 15px;
          margin-top: 15px;
     }
</style>
