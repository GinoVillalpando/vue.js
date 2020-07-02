<template>
    <v-app-bar max-height="100%" :absolute="true" dark fixed app>
        <v-toolbar-title>To-do App :D</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-menu>
          <template v-slot:activator="{ on, attrs }">
            <v-app-bar-nav-icon v-bind="attrs" v-on="on" slot="activator" />
          </template>
          <v-list>
            <v-list-item v-for="item in menu" :key="item.id" :to="item.link">
              <v-list-item-title>{{ item.name }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
    </v-app-bar>
</template>

<script>
export default {
  data: () => ({
    menu: [
      {
        id: 1,
        name: "home",
        link: "home"
      },
      {
        id: 2,
        name: "social",
        link: "social"
      },
      {
        id: 3,
        name: "blog",
        link: "blog"
      },
    ]
  }),
  name: 'Header',
  props: {
    msg: String,
    about: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
