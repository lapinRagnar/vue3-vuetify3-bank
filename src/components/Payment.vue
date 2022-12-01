<template>
  <v-row>

    <v-col cols="12" sm="6">

      <v-toolbar color="transparent" >

        <v-toolbar-title>All Payment</v-toolbar-title>
        <v-chip color="green">2</v-chip>

      </v-toolbar>

      <v-row>

        <v-col cols="12" sm="6">
          <v-card color="#242426" class="rounded-lg mx-2 pa-2">
            <span class="text-caption text-grey ">Credit Card</span> <br>
            <h6>Balance</h6>
            <h4>451 121 €</h4>
            <v-card-text class="pt-0">
              <v-icon color="grey" class="mr-2">fab fa-cc-mastercard </v-icon>
              <span class="text-caption text-grey font-weight-light">**********542154</span>
            </v-card-text>
          </v-card>
        </v-col>

        <v-col cols="12" sm="6">
          <v-card color="#242426" class="rounded-lg mx-2 pa-2">
            <span class="text-caption text-grey ">Credit Card</span> <br>
            <h6>Balance</h6>
            <h4>- 20 121 €</h4>
            <v-card-text class="pt-0">
              <v-icon color="grey" class="mr-2">fab fa-cc-visa </v-icon>
              <span class="text-caption text-grey font-weight-light">**********542154</span>
            </v-card-text>
          </v-card>
        </v-col>

      </v-row>

    </v-col>

    <v-col cols="12" sm="6">

      <v-toolbar color="transparent" variant="flat">
        <v-toolbar-title>All Transactions</v-toolbar-title>
        <v-chip color="green">12</v-chip>
      </v-toolbar>

      <v-card color="#242426" class="rounded-lg mr-2 ">

        <h5>Recent Experiances</h5>

        <v-list color="transparent">
          <v-list-item
            v-for="(experiance, i) in experiances"
            :key="i"
            :subtitle="experiance.subtitle"
            :title="experiance.title"
          >

          <template v-slot:append>



            <v-list-item-action>
              <h5>{{ experiance.price }}</h5>
              <v-btn>
                <v-icon color="grey">fas fa-chevron-right</v-icon>
              </v-btn>
            </v-list-item-action>

            <v-avatar rounded="0">
              <v-img :src="experiance.img"></v-img>
            </v-avatar>


          </template>



          </v-list-item>
        </v-list>
      </v-card>

    </v-col>


  </v-row>
</template>

<script setup>

  import { ref } from 'vue';


  const experiances = ref([
    {
      img: "spotify.png",
      subtitle: "Premium 1 Month Service",
      title: "Spotify",
      price: "-$49.59",
    },
    {
      img: "netflix.png",
      subtitle: "Premium 1 Month Service ",
      title: "Netflix",
      price: "-$106.58",
    },
  ])

</script>

<style lang="scss">

</style>

<i class="fa-brands fa-spotify"></i>
