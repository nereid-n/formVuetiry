<template>
  <v-navigation-drawer
      fixed
      :value="drawer"
      app
  >
    <v-list dense>
      <v-list-tile v-for="item in items"
                   :to="item.to"
                   :key="item.name"
      >
        <v-list-tile-content>
          <v-list-tile-title>{{item.name}}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
  export default {
    name: "Navigation",
    data: () => ({
      items: [
        {
          name: 'Объявления',
          to: '/cabinet/ads'
        },
        {
          name: 'Добавить объявление',
          to: '/cabinet/ad/add'
        },
        {
          name: 'Профиль',
          to: '/cabinet/profile'
        },
        {
          name: 'Аккаунт',
          to: '/cabinet/account'
        },
        {
          name: 'Соцсети',
          to: '/cabinet/networks'
        }
      ]
    }),
    props: {
      drawer: {
        required: true
      }
    }
  }
</script>

<style scoped>
  .v-navigation-drawer {
    z-index: 5;
  }
</style>