<template>
     <header>
          <h1>Vue Tasks v{{ version }}</h1>
          <Button text="Add Task" color="lime"/>
     </header>
</template>

<script>
     import Button from './Button.vue'

     export default {
          name: 'Header',
          props: {
               version: String
          },
          components: {Button}
     }
</script>

<style scoped>
     header {
          display: flex;
          justify-content: space-around;
          align-items: center;

          border: 1px solid black;
          border-radius: 10px;
          padding: 10px;
          margin: 5px;
     }
</style>