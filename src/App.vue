<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          :src="image_src"
          transition="scale-transition"
          width="50"
        />

      </div>

      <v-spacer></v-spacer>

        <span class="mr-2 font-weight-bold">スマコン</span>
        
      
    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
    image_src: require("/Users/canon/workspace/vue/smash/src/assets/mini.png")
  
  }),
};
</script>
