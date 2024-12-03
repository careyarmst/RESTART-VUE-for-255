<template>
 <v-app>
  <v-toolbar app>
  </v-toolbar>
  <v-content>
    <br>
    <NewMessage/>  
    <br>
    <messagesMWord/>
  </v-content>
    
 </v-app>
</template>

<script>
import messagesMWord from './components/messagesMword';
import NewMessage from './components/NewMessage';

export default {
  name: 'App',

  components: {
    messagesMWord, NewMessage
  },

  data: () => ({
    //
  }),
};
</script>
