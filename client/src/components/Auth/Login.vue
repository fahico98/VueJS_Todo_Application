
<template>
   <v-container>
      <v-layout align-center justify-center>
         <v-flex xs12 sm8 md4>
            <v-form>
               <v-card outlined>
                  <v-card-text>
                     <span class="display-1 red--text text--darken-4">Login form</span>
                     <v-text-field name="username" label="Username" type="text" color="red darken-4"></v-text-field>
                     <v-text-field name="password" label="Password" type="password" color="red darken-4"></v-text-field>
                  </v-card-text>
                  <v-divider></v-divider>
                  <v-card-actions>
                     <v-btn type="submit" tile dark class="elevation-0 text-capitalize" color="red darken-4">Sign in</v-btn>
                     <v-btn type="button" tile dark class="elevation-0 text-capitalize" color="grey darken-1">Cancel</v-btn>
                  </v-card-actions>
               </v-card>
            </v-form>
         </v-flex>
      </v-layout>
   </v-container>
</template>

<script>

   export default {
      name: "login"
   }
   
</script>
