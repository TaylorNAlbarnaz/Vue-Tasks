<template>
     <header>
          <h1>Vue Tasks v{{ version }}</h1>
          <Button text="Add Task" color="limegreen"/>
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

          margin-bottom: 15px;
     }
</style>