
<template>
   <v-navigation-drawer permanent style="width: 100%; overflow: hidden">
      <v-toolbar dark color="red darken-4 elevation-0">
         <v-toolbar-title>Opstions list</v-toolbar-title>
         <v-spacer></v-spacer>
         <v-btn type="button" tile dark class="elevation-0 text-capitalize" color="grey darken-1">search</v-btn>
      </v-toolbar>
      <v-list>
         <v-list-tile color="grey darken-1">

            <v-list-tile-content>
               <v-list-tile-title>Create a new list</v-list-tile-title>
            </v-list-tile-content>
            
            <v-list-tile-action>
               <v-list-tile-title>
                  <v-btn type="button" tile dark class="elevation-0 text-capitalize" color="grey darken-1">add</v-btn>
               </v-list-tile-title>
            </v-list-tile-action>

         </v-list-tile>
      </v-list>
      <v-divider></v-divider>
      <v-list>
         
      </v-list>
   </v-navigation-drawer>
</template>

<script>

   export default {
      name: "todo-list"
   }

</script>
