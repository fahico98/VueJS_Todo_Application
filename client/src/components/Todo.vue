
<template>
   <v-container fluid fill-height py-0>
      <v-layout row align-space-between justify-space-between>
         <v-flex lg3 pr-1>
            <list/>
         </v-flex>
         <v-flex lg6 px-1>
            <list/>
         </v-flex>
         <v-flex lg3 pl-1>
            <list/>
         </v-flex>
      </v-layout>
   </v-container>
</template>

<script>

   import list from "./List";

   export default {
      name: "todo",
      components: {
         list
      }
   }

</script>
