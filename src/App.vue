<template>
  <v-app app>
    <!-- <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Vuetify</span>
        <span class="font-weight-light">MATERIAL DESIGN</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>fas fa-external-link-alt</v-icon>
      </v-btn>
    </v-app-bar> -->
 <v-navigation-drawer
    app
    permanent
    left
    color="blue-grey darken-4"
  >
    <template v-slot:prepend>
      <v-row class="ml-5" align="center" justify="center">
        <v-col cols="12" align-self="center">
          <v-avatar size="164">
            <img :style="`border:5px solid #607d8b !important`" :src="require('@/assets/IMG_20191126_082725.jpg')">
          </v-avatar>
        </v-col>
        <v-col cols="12" align-self="center">
          <span class="white--text headline font-weight-bold">
            Miguel Villamizar
          </span>
        </v-col>
      </v-row>
    </template>

        <v-divider></v-divider>

        <v-list dense>
          <v-list-item
            dark
            :href="item.link ? item.link : '#'"
            color="white"
            v-for="item in items"
            :key="item.title"
          >
            <v-list-item-icon class="mr-1">
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
    </v-navigation-drawer>
    <v-content>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  data(){
    return {
      items:[
        {
          link: "https://www.linkedin.com/in/miguel-villamizar-9b653a145/",
          icon: "fab fa-linkedin-in",
          title: "/miguel-villamizar-9b653a145/"
        },
        {
          link: "https://conan4069.gitlab.io/",
          icon: "fab fa-gitlab",
          title: "@conan4069"
        },
        {
          link: "https://conan4069.github.io/",
          icon: "fab fa-github",
          title: "@conan4069"
        },
        {
          link: "#",
          icon: "fa fa-user",
          title: "+58 412 078 0581"
        },
      ]
    }
  },
};
</script>
