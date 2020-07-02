<template>
  <v-app>
    <Header msg="Home"/>
    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Header from './components/Header'

export default {
  name: 'App',

  components: {
    HelloWorld,
    Header
  },

  data: () => ({
    //
  }),
};
</script>
