<template>
  <div>
    <v-container>
      <v-layout text-xs-center wrap align-center>
        <v-flex xs12 sm8 lg6 mb-5>
          <v-carousel hide-delimiters>
            <v-carousel-item
              v-for="(item, i) in items"
              :key="i"
              :src="item.src"
            ></v-carousel-item>
          </v-carousel>
        </v-flex>

        <v-flex xs12 sm4 lg6>
          <h1 class="display-2 font-weight-bold mb-3 text-uppercase">
            Meet Product
          </h1>
          <p class="subheading font-weight-regular text-uppercase">
            The best Generic product there is!
          </p>
        </v-flex>

        <v-flex mb-5 md10 offset-md2>
          <p class="headline text-md-right">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Harum
            maiores modi quidem veniam, expedita quis laboriosam, ullam facere
            adipisci, iusto, voluptate sapiente corrupti asperiores rem nemo
            numquam fuga ab at.
          </p>
        </v-flex>
      </v-layout>
    </v-container>
    <v-container fluid class="teal lighten-5">
      <Advantages />
    </v-container>
    <v-container fluid class="teal lighten-4">
      <Description />
    </v-container>
    <v-container fluid class="teal lighten-5">
      <Feedback />
    </v-container>
  </div>
</template>

<script>
import Advantages from "./Advantages";
import Feedback from "./Feedback";
import Description from "./Description";

export default {
  data: () => ({
    items: [
      {
        src: "https://picsum.photos/600/800/?random"
      },
      {
        src: "https://picsum.photos/605/805/?random"
      },
      {
        src: "https://picsum.photos/610/810/?random"
      }
    ]
  }),
  components: { Advantages, Feedback, Description }
};
</script>

<style></style>
