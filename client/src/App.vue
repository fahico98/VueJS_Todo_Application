
<template>
   <v-app>
      <todo/>
   </v-app>
</template>

<script>
   
   import todo from "./components/Todo"

   export default {
      name: "app",
      components: {
         todo
      }
   };

</script>
