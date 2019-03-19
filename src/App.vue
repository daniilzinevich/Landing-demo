<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Product</span>
        <span class="font-weight-light">Generic product</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        flat
        @click="
          $vuetify.goTo('#contact-us', {
            duration: 900,
            easing: 'easeInOutQuad'
          })
        "
      >
        <span class="mr-2">Contact us</span>
      </v-btn>
    </v-toolbar>

    <v-content>
      <HelloWorld />
    </v-content>
    <Footer />
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Footer from "./components/Footer";

export default {
  name: "App",
  components: {
    HelloWorld,
    Footer
  },
  data() {
    return {
      //
    };
  }
};
</script>
