<template>
  <v-app>
   <v-container class="login_card_center">
     <v-row>
       <v-col  md="6" offset-md="3">
         <v-card>
           <v-card-title class="">
             <h3 >User Login</h3>
           </v-card-title>
           <v-card-text>
             <v-text-field
              label="User Name"
              prepend-icon="mdi-account-circle"
            >
            </v-text-field>
             <v-text-field
              label="Password"
              :type="showPassword ? 'text' : 'password' "
              prepend-icon="mdi-lock"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off' "
              @click:append="showPassword = !showPassword "
            >
            </v-text-field>
           </v-card-text>
           <v-divider></v-divider>
           <v-card-actions>
             <v-btn class="primary">Login</v-btn>
           </v-card-actions>
         </v-card>
       </v-col>
     </v-row>
   </v-container>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
      showPassword:false,
  }),
};
</script>
<style scoped>
.login_card_center{
  position: relative;
  top:50%;
  left:50%;
  transform: translate(-50%,-50%);
}
</style>