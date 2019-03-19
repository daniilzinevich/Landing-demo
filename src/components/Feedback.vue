<template>
  <v-layout>
    <v-flex xs12 md6 offset-md3>
      <v-form id="contact-us">
        <v-container>
          <v-layout wrap>
            <v-flex xs12>
              <h2 class="headline text-xs-center">
                Like our product? Give us more info to contact you later
              </h2>
            </v-flex>
            <v-flex xs12 sm6>
              <v-text-field
                v-model="firstname"
                :rules="nameRules"
                :counter="10"
                label="First name"
                required
              ></v-text-field>
            </v-flex>
            <v-flex xs12 sm6>
              <v-text-field
                v-model="email"
                :rules="emailRules"
                label="E-mail"
                required
              ></v-text-field>
            </v-flex>
            <v-flex xs12 mb-3>
              <v-textarea
                name="input-7-1"
                label="Additional info"
                v-model="additional"
                hint="Give us some details"
              ></v-textarea>
            </v-flex>
            <v-layout justify-center wrap>
              <v-btn>submit</v-btn>
            </v-layout>
          </v-layout>
        </v-container>
      </v-form>
    </v-flex>
  </v-layout>
</template>
<script>
export default {
  data() {
    return {
      firstname: "",
      lastname: "",
      nameRules: [
        v => !!v || "Name is required",
        v => v.length <= 10 || "Name must be less than 10 characters"
      ],
      email: "",
      emailRules: [
        v => !!v || "E-mail is required",
        v => /.+@.+/.test(v) || "E-mail must be valid"
      ],
      additional: ""
    };
  }
};
</script>
