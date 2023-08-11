<template>
     <button @click="onClick()" :style='{ background: color }'>{{ text }}</button>
</template>

<script>
     export default {
          name: 'Button',
          props: {
               text: String,
               color: String
          },
          methods: {
               onClick() {
                    alert('clicked')
               }
          }
     }
</script>

<style scoped>
     button {
          border: 0;
          border-radius: 5px;
          padding: 10px 20px;
          color: white;
          font-weight: bold;
          cursor: pointer;
     }

     button:hover {
          opacity: 0.7;
     }

     button:active {
          opacity: 0.5;
     }
</style>