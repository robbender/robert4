<template>
    <div id="">
  <v-app id="">
    <H1>Contact Me</H1>
    <br>
    <v-form v-model="valid">
      <v-container>
        <v-layout>
          <v-flex
            xs12
            md4
          >
            <v-text-field
              v-model="firstname"
              :rules="nameRules"
              :counter="10"
              label="First name"
              required
            ></v-text-field>
          </v-flex>
  
          <v-flex
            xs12
            md4
          >
            <v-text-field
              v-model="lastname"
              :rules="nameRules"
              :counter="10"
              label="Last name"
              required
            ></v-text-field>
          </v-flex>
  
          <v-flex
            xs12
            md4
          >
            <v-text-field
              v-model="email"
              :rules="emailRules"
              label="E-mail"
              required
            ></v-text-field>
          </v-flex>
        </v-layout>
      </v-container>
      <v-container fluid grid-list-md>
      <v-textarea
        name="input-7-1"
        box
        label="Your message:"
        auto-grow
        value=""
      ></v-textarea>
    </v-container>
    </v-form>
  </v-app>
</div>
</template>

<script>
// import { Script } from 'vm';

export default {
  name: 'Contract',

  data: () => ({
    valid: false,
    firstname: '',
    lastname: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => v.length <= 10 || 'Name must be less than 10 characters'
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+/.test(v) || 'E-mail must be valid'
    ]
  })
}

</script>
