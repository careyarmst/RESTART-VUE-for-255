<template>
    <v-flex sm8 offset-sm2>
      <v-card>
       <v-toolbar dark>
         <v-toolbar-title>Messages</v-toolbar-title>
         </v-toolbar>
       <v-list>
          <v-list-item v-for="(message, index) in $store.state.messages" :key="index">
             <v-list-item-content>
                <v-list-item-title>{{ message }}</v-list-item-title>
             </v-list-item-content>
          </v-list-item>
       </v-list>
      </v-card>
   </v-flex>
 </template>
  <script>
 import axios from 'axios'
     export default {
       data() {
          return {
 
          };
       },
       async created() {
         
         this.$store.state.messages = (await axios.get('http://localhost:3000/messages')).data

                }
    };
 </script>
