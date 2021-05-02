<template>
  <v-form ref="form" lazy-validation class="margin-x-150 py-md-16 py-8 my-5">
    <v-container fluid>
      <v-row>
        <v-col
          cols="12"
          md="6"
        >
          <v-text-field
            v-model="firstname"
            :rules="nameRules"
            type="text"
            label="Your Name"
            color="#7549FF"
            validate-on-blur
            required
          ></v-text-field>
        </v-col>
        <v-col
          cols="12"
          md="6"
        >
          <v-text-field
            v-model="email"
            :rules="emailRules"
            type="email"
            label="E-mail"
            color="#7549FF"
            validate-on-blur
            required
          ></v-text-field>
        </v-col>
        <v-col
          cols="12"
          md="12"
          class="mt-5"
        >
          <v-textarea
            v-model="message"
            :rules="nameRules"
            type="text"
            label="Message"
            color="#7549FF"
            validate-on-blur
            required
          ></v-textarea>
        </v-col>
        <v-btn
            class="white--text mt-3 mb-5 px-10 py-6"
            color="#7549FF"
            @click.prevent="submit"
            type="submit"
          >
            Submit
        </v-btn>
        <v-snackbar
          v-model="snackbar"
          color="success darken-5"
          timeout="2000"
        >
          <p class="pa-0 ma-0"><v-icon class="mr-2">mdi-check</v-icon> Email Sent Successfully</p>
        </v-snackbar>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
export default {
  data: () => ({
    firstname: '',
    message: '',
    snackbar:false,
    nameRules: [
      v => !!v || 'Name is required',
      v => v.length <= 15 || 'Name must be less than 15 characters',
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+/.test(v) || 'E-mail must be valid',
    ],
  }),
  methods:{
    submit(){
      if(this.$refs.form.validate()){
        this.snackbar=true
        this.firstname=''
        this.email=''
        this.message=''
      }
    }
  }
}
</script>
