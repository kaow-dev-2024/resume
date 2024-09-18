<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app>
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact color="primary">
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped"  dense fixed app >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-spacer></v-spacer>
      <div>
        <v-list-item two-line>
          <v-list-item-content>
            <v-list-item-title>
              JA
            </v-list-item-title>
            <v-list-item-subtitle>
              Jajetsata Thongklieng
            </v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </div>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

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
          icon: 'mdi-account-circle',
          title: 'Personal Information',
          to: '/'
        },
        {
          icon: 'mdi-school',
          title: 'Education',
          to: '/education'
        },
        {
          icon: 'mdi-account-hard-hat',
          title: 'Work Experience',
          to: '/work-experience'
        },
        {
          icon: 'mdi-account-details',
          title: 'Skills',
          to: '/skills'
        },

      ],



      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',

    }
  },



  methods: {
    async getTitleBar(item) {
      let itemTitle = await Object.assign({}, item)
      console.log('itemTitle', itemTitle);
      this.titleBar = await itemTitle.title
    }
  },
}
</script>
