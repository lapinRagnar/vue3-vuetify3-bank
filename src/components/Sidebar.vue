<template>


  <v-navigation-drawer
    color="#524eed"
    rail
    v-model="drawer"
    rail-width="65"
  >
    <v-list>
      <v-list-item      >
        <v-icon size="x-large">fab fa-instalod</v-icon>
      </v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list
      :items="items"
    >
    </v-list>



    <v-list>



    </v-list>


    <div style="position: absolute; bottom: 0;" >

      <v-list-item>
        <v-btn color="transparent" size="25">
          <v-icon>fas fa-cog</v-icon>
        </v-btn>
      </v-list-item>

      <v-list-item>
        <v-btn color="transparent" size="25" >
          <v-icon>fas fa-sign-out-alt</v-icon>
        </v-btn>
      </v-list-item>

    </div>

  </v-navigation-drawer>


</template>

<script setup>

  import { ref } from 'vue';

  const selectItem = ref(0)
  const model = ref(1)
  const drawer = ref(null)


  const items = ref([
    {
      title: '',
      value: 1,
      props: {
        prependIcon: 'fas fa-bars'
      }
    },
    {
      title: '',
      value: 2,
      props: {
        prependIcon: 'far fa-compass'
      }
    },
    {
      title: '',
      value: 3,
      props: {
        prependIcon: 'fas fa-wallet'
      }
    },
    {
      title: '',
      value: 4,
      props: {
        prependIcon: 'far fa-comment-dots'
      }
    },
    {
      title: '',
      value: 5,
      props: {
        prependIcon: 'far fa-calendar-alt'
      }
    },
    {
      title: '',
      value: 6,
      props: {
        prependIcon: 'far fa-file-alt'
      }
    },
  ])

  // *************************************
  // const items = ref([
  //   {
  //     props: {
  //       prependIcon: 'fas fa-bars'
  //     }
  //   },
  //   {
  //     props: {
  //       prependIcon: 'far fa-compass'
  //     }
  //   },
  //   {
  //     props: {
  //       prependIcon: 'fas fa-wallet'
  //     }
  //   },
  //   {
  //     props: {
  //       prependIcon: 'far fa-comment-dots'
  //     }
  //   },
  //   {
  //     props: {
  //       prependIcon: 'far fa-calendar-alt'
  //     }
  //   },
  //   {
  //     props: {
  //       prependIcon: 'far fa-file-alt'
  //     }
  //   },
  // ])

  // *************************************


  // const items = ref([
  //   {icon: 'fas fa-bars'},
  //   {icon: 'far fa-compass'},
  //   {icon: 'fas fa-wallet'},
  //   {icon: 'far fa-comment-dots'},
  //   {icon: 'far fa-calendar-alt'},
  //   {icon: 'far fa-file-alt'},
  // ])

  // *************************************

  // const items = ref([
  //   {
  //     title: 'Item #1',
  //     value: 1,
  //     props: {
  //       prependIcon: 'mdi:mdi-home',
  //     },
  //   },
  //   {
  //     title: 'Item #2',
  //     value: 2,
  //     props: {
  //       appendIcon: 'mdi:mdi-close',
  //     },
  //   },
  //   {
  //     title: 'Item #3',
  //     value: 3,
  //     props: {
  //       color: 'red',
  //       appendIcon: 'mdi:mdi-close',
  //     },
  //   },
  // ])

</script>

<style lang="scss">
  .border {
    margin-left: 12px;
    margin-right: 12px;
    background: #524eed;
    border-radius: 50%;
    text-decoration: none;
  }

  .v-list-item-group .v-list-item--active {
    color: white !important;
  }
</style>
