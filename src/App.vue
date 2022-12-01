<template>


  <v-app id="inspire" theme="dark">

    <Sidebar />

    <v-container>
      <Navbar />
      <v-row>

        <v-col cols="12" sm="8">

          <v-row>

            <v-col cols="12" sm="12">
              <Overview />
            </v-col>

            <v-col cols="12" sm="12">
              <Money />
            </v-col>

            <v-col cols="12" sm="12">
              <Payment />
            </v-col>

          </v-row>
        </v-col>

        <v-col cols="12" sm="4">
          <Card />
        </v-col>

      </v-row>

    </v-container>

  </v-app>

</template>

<script setup>

  import { useTheme } from 'vuetify'
  import { useAuthStore } from '@/stores/auth'


  import Sidebar from '@/components/Sidebar.vue'
  import Navbar from '@/components/Navbar.vue'
  import Overview from '@/components/Overview.vue'
  import Money from '@/components/Money.vue'
  import Payment from '@/components/Payment.vue'
  import Card from '@/components/Card.vue'
  import { onMounted, ref } from 'vue'

  onMounted(() => {
    const theme = useTheme()
    console.log('theme', theme)
  })

  const authStore = useAuthStore()
  console.log('authStore', authStore.maVariablePinia)

  const drawer = ref(null)

</script>

<style lang="scss">

  .v-btn.without-uppercase {
    text-transform: none !important;
  }

  .v-btn:not(.v-btn--round).v-size--small {
    min-width: 30px !important;
    padding: 0 5px !important;
  }

</style>
