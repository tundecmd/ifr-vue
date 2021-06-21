<template>
  <v-app>
  <v-app-bar
    app
    color="yellow"
  >
    <v-toolbar-title class="blue--text">
      <router-link to="/" text class="text-decoration-none">
      <v-btn 
        text
        class="blue--text text-uppercase text-h4"
      >
        IFARA
      </v-btn>
    </router-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <router-link to="/" text class="text-decoration-none">
      <v-btn 
        text
        class="blue--text text-capitalize text-h5"
      >
        Home
      </v-btn>
    </router-link>
    <router-link to="/about" text class="text-decoration-none">
      <v-btn 
        text
        class="blue--text text-capitalize text-h5"
      >
        About Us
      </v-btn>
    </router-link>
    <!-- <router-link to="/about" text class="blue--text">About Us</router-link> -->
  </v-app-bar>
  <v-content>
    <router-view></router-view>    
  </v-content>
  
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      width="100%"
      class="yellow blue--text text-center"
    >
      <v-card-text class="my-5 blue--text pt-0 pb-0">
        Suite 20, Oadis plaza, 4 CMD road, Ikosi-GRA, Lagos
        Phone: 234(0)8071914351
      </v-card-text>
      <v-card-text class="blue--text pt-0 font-italic">
        info@ifarabooks.com
      </v-card-text>
      <v-card-text class="blue--text pt-0">
        Open Hours:
        Mon-Fri: 9:00am - 5:00am
        Sat - Sun: CLOSED
      </v-card-text>
      <v-card-text 
        class="mx-4 blue--text"
      >
        <a
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-4 blue--text text-decoration-none"
          icon
          :href="icon.urlLink"
          target="_blank" 
          rel="noopener noreferrer"
        >
          <v-icon size="24px" class="mx-4 blue--text">
            {{ icon.logo }}
          </v-icon>
        </a>
      </v-card-text>
    </v-card>
  </v-footer>
  </v-app>
</template>

<script>

export default {

  
  name: 'App',

  data: () => ({ 
    //
    slides: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
        ],
    icons: [
      {
        logo: 'mdi-facebook',
        urlLink: 'https://www.facebook.com'
      },
      {
        logo: 'mdi-twitter',
        urlLink: 'https://www.facebook.com'
      },
      {
        logo: 'mdi-linkedin',
        urlLink: 'https://www.linkedin.com/'
      },
      {
        logo: 'mdi-instagram',
        urlLink: 'https://www.instagram.com/'
      }
    ]
  })
};
</script>
