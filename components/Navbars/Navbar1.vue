<template>
  <div class="d-flex flex-row justify-space-between px-md-12 px-6 fixed-top" id="navigation">
    <v-navigation-drawer
      v-model="drawer"
      absolute
      height="100vh"
      id="drawer"
    >
      <v-list-item class="mt-4">
        <v-list-item-content>
          <v-list-item-title class="font-weight-bold h1">Luna.</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider class="mt-0"></v-divider>
      <v-list>
      <v-list-group
        v-for="menu in menus"
        :key="menu.id"
        v-model="menu.active"
        :prepend-icon="menu.icon2"
        no-action
        class="mb-4"
        append-icon="mdi-chevron-down"
      >
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title v-text="menu.title"></v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item
          v-for="link in menu.links"
          :key="link.item"
        >
          <v-list-item-content>
            <v-list-item-title><nuxt-link :to="link.route" class="drawer-links">{{link.item}}</nuxt-link></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-group>
    </v-list>
    </v-navigation-drawer>
    <h1 class="white--text mt-3">Luna.</h1>
    <div class="mt-4 d-md-inline-block d-none">
      <v-menu
        offset-y
        v-for="menu in menus"
        :key="menu.id"
        transition="slide-y-transition"
      >
        <template v-slot:activator="{ attrs, on }" >
            <a
            class="grey--text text--lighten-4 pa-4 text-uppercase paragraphs3 titles"
            v-bind="attrs"
            v-on="on"
          >
            {{menu.title}}
            <v-icon small class="grey--text text--lighten-4">mdi-chevron-down</v-icon>
          </a>
        </template>
        <v-list class="list-background ma-0 pa-0" flat>
          <v-list-item
            v-for="link in menu.links"
            :key="link.item"
            link
            class="pr-16"
          >
            <v-list-item-title><nuxt-link :to="link.route" class="white--text list-items">{{link.item}}</nuxt-link></v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </div>
    <div class="mt-3 d-sm-block d-none">
      <v-icon class="white--text paragraphs4 icons">mdi-facebook</v-icon>
      <v-icon class="white--text ml-6 paragraphs4 icons">mdi-twitter</v-icon>
      <v-icon class="white--text ml-6 paragraphs4 icons">mdi-instagram</v-icon>
      <v-icon class="white--text ml-6 paragraphs4 icons">mdi-linkedin</v-icon>
    </div>
    <div class="mt-3 d-md-none d-inline-block burger-icon" v-if="drawer" @click="drawer=!drawer">
      <v-icon class="white--text icons">mdi-menu</v-icon>
    </div>
    <div class="mt-3 d-md-none d-inline-block burger2" v-else @click="drawer=!drawer">
      <v-icon class="white--text icons ">mdi-menu</v-icon>
    </div>

  </div>

</template>

<style lang="sass" scoped>
@import "~/assets/style.sass"
#navigation
  @include transition(all, 0.2s, ease-in-out)
.drawer-links
  color: rgba(0, 0, 0, 0.8) !important
.burger-icon
  height: 100vh
.list-background
  background: rgba(22,22,23,0.9) !important
  .list-items
    @include transition(all, 0.3s, ease-in-out)
    &:hover
      color: $main-color !important

h1
  font-weight: 700
  font-size: 32px
  @media (max-width: 575.98px)
    font-size: 24px
  @media (min-width: 576px) and (max-width: 767.98px)
    font-size: 26px
  @media (min-width: 768px) and (max-width: 991.98px)
    font-size: 28px
a
  border: none !important
  text-decoration: none !important
  letter-spacing: 1.2px
.v-menu__content
  margin-top: 10px
.icons
  cursor: pointer
  @include transition(all, 0.3s, ease-in-out)
  &:hover
    color: $main-color !important
</style>

<script>
export default {
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll);
  },
  mounted(){
    window.addEventListener('resize',function(){
      if(this.drawerHeight==true && window.innerWidth<1000){
        document.getElementById("drawer").style.transform="translateX(0%)"
      }else{

      }
       if(window.innerWidth>1000){
        document.getElementById("drawer").style.transform="translateX(-100%)"
      }
    })
  },
  data: () => ({
    drawerHeight:false,
    drawer: false,
    menus:[
      {
        id:0,
        active: false,
        title:'Home',
        links:[
          {
            item:'Agency',
            route:'/'
          },
          {
            item:'Business',
            route:'/business'
          },
          {
            item:'Freelance',
            route:'/freelance'
          },
        ],
        icon2:'mdi-home',
      },
      {
        id:1,
        title:'Pages',
        links:[
          {
            item:'Services',
            route:'/headings'
          },
          {
            item:'Portfolio',
            route:'/agency'
          },
          {
            item:'Comming Soon',
            route:'/soon'
          },
        ],
        icon2:'mdi-book-open-page-variant'
      },
      {
        id:2,
        title:'Blog',
        links:[
          {
            item:'Blog List',
            route:'/agency'
          },
          {
            item:'Blog Sidebar',
            route:'/business'
          },
        ],
        icon2:'mdi-blogger'
      },
      {
        id:3,
        title:'Shortcodes',
        links:[
          {
            item:'Buttons',
            route:'/buttons'
          },
          {
            item:'Headings',
            route:'/headings'
          },
        ],
        icon2:'mdi-xml'
      },
      {
        id:4,
        title:'Contacts',
        links:[
          {
            item:'Contacts 1',
            route:'/contacts1'
          },
          {
            item:'Contacts 2',
            route:'/contacts2'
          },
        ],
        icon2:'mdi-account-box'
      }
    ]
  }),
  methods:{
    handleScroll(){
      if(window.scrollY>100){
        document.getElementById('navigation').style.display= "none"
        document.getElementById('navigation').classList.remove("d-flex")
      }else{
        document.getElementById('navigation').style.display= "block"
        document.getElementById('navigation').classList.add("d-flex")
      }
    }
  }
}
</script>
