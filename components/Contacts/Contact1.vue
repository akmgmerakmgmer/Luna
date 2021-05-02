<template>
  <div class="background text-center py-16">
    <h4 class="white--text font-weight-bold">Offer your project to Luna's Team</h4>
    <v-dialog v-model="dialog" width="600">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          class="button px-12 py-7 text-subtitle-1 mt-8"
          dark
          v-bind="attrs"
          v-on="on"
          retain-focus-on-click
        >
          LET'S TALK
        </v-btn>
      </template>
      <v-card class="px-5 py-10">
        <v-form
        ref="form"
        lazy-validation
        >
          <v-text-field
            :rules="nameRules"
            v-model="name"
            label="Name"
            required
            type="text"
            color="#7549FF"
            prepend-icon="mdi-rename-box"
            validate-on-blur
          ></v-text-field>
          <v-text-field
            :rules="emailRules"
            v-model="email"
            label="E-mail"
            required
            type="email"
            color="#7549FF"
            prepend-icon="mdi-email"
            validate-on-blur
          ></v-text-field>
          <v-textarea
            :rules="textArea"
            label="Description"
            v-model="textarea"
            required
            type="text"
            color="#7549FF"
            prepend-icon="mdi-card-text"
            validate-on-blur
          ></v-textarea>
          <v-btn
            class="white--text mt-6 mb-2"
            color="#7549FF"
            @click.prevent="submit"
            type="submit"
          >
            Submit
          </v-btn>
        </v-form>
      </v-card>
    </v-dialog>
    <v-snackbar
      v-model="snackbar"
      color="success darken-5"
      timeout="2000"
    >
      <p class="pa-0 ma-0"><v-icon class="mr-2">mdi-check</v-icon> Email Sent Successfully</p>
    </v-snackbar>
  </div>
</template>

<style lang="sass" scoped>
@import "~/assets/style.sass"
.background
  background: $main-color !important
  .button
    background: #7549FF !important
    border-radius: 25px
    font-weight: 600
    box-shadow: 2px 2px 15px 2px rgba(0, 0, 0, 0.3)
    letter-spacing: 5px !important
    &:hover
      box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.3)
</style>

<script>
export default {
  data(){
    return{
      name:'',
      email:'',
      textarea:'',
      dialog:false,
      snackbar:false,
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 15) || 'Name must be less than 10 characters',
      ],
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'Please Enter a Valid Email',
      ],
      textArea:[
        v => !!v || 'Description is required',
      ]
    }
  },
  methods:{
    submit(){
      if(this.$refs.form.validate()){
        this.dialog=false
        this.snackbar=true
        this.name=''
        this.email=''
        this.textarea=''
      }
    }
  }
}
</script>
