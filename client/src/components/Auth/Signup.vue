
<template>
   <v-container>
      <v-layout align-center justify-center>
         <v-flex xs12 sm8 md6>
            <v-card outlined>
               <v-form>
                  <v-card-text>
                     <span class="display-1 red--text text--darken-4">Signup form</span>
                     <v-alert type="error">This user already exists...!</v-alert>
                     <v-text-field name="username" label="Username" type="text" color="red darken-4"
                        v-model="username" :rules="[rules.required]"></v-text-field>
                     <v-text-field name="email" label="E-mail" type="text" color="red darken-4"
                        v-model="email" :rules="[rules.required, rules.email]"></v-text-field>
                     <v-text-field name="password" label="Password" type="password" color="red darken-4"
                        v-model="password" :rules="[rules.required]"></v-text-field>
                     <v-text-field name="password" label="Confirm password" type="password" color="red darken-4" 
                        v-model="confirm_password" :rules="[rules.required]" :error="!valid()"></v-text-field>
                  </v-card-text>
                  <v-divider></v-divider>
                  <v-card-actions>
                     <v-btn type="submit" tile dark class="elevation-0 text-capitalize" color="red darken-4">Sign in</v-btn>
                     <v-btn type="button" tile dark class="elevation-0 text-capitalize" color="red darken-4">Register</v-btn>
                  </v-card-actions>
               </v-form>
            </v-card>
         </v-flex>
      </v-layout>
   </v-container>
</template>

<script>

   export default {
      name: "signup",
      data: () => ({
         userExists: false,
         username: '', 
         email: '',
         password: "",
         confirm_password: "",
         rules: {
            required: value => !!value || "Required",
            email: value => {
               const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
               return pattern.test(value) || "Invalid e-mail.";
            }
         }
      }),
      methods: {
         valid(){
            return this.password === this.confirm_password;
         }
      }
   }

</script>
