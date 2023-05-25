<template>
  <v-app dark>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
      <!-- <v-footer class="d-flex justify-center" :absolute="!fixed" app>
      
      </v-footer> -->
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {

      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
<style>
* {
  font-family: 'boonhome';
  color: #169fc6;
}
#btn {
  font-family: 'boonhome';
  color: #fff;
}

@font-face {
  font-family: 'boonhome';
  font-style: normal;
  font-weight: 400;
  font-display: swap;
  src: url('~assets/boonhome.otf') format('truetype');
}
html {
  font-family: 'boonhome';
}

</style>

