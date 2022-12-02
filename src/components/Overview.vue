<template>
  <v-card
    color="#202022"
    class="mt-10 rounded-lg"
    flat
  >
    <v-row >
      <v-col cols="12" sm="4" class="pa-10">
        <v-card color="transparent" class="rounded-lg mx-2">
          <v-btn color="green" size="small">
            <v-icon color="white">fa-solid fa-euro-sign</v-icon>
          </v-btn>
          <h2>5 485,55 €</h2>
          <h6 class="text-grey">Available Ballance</h6>
          <v-btn color="#524eed" class="without-uppercase">Link Accounts</v-btn>
        </v-card>
      </v-col>

      <v-col cols="12" sm="4" class="pa-10">
        <v-card color="#242426" class="rounded-lg mx-2 pa-5">
          <v-toolbar color="rgba(0, 0, 0, 0)" class="mt-n7">
            <span class="caption text-grey" >Sales</span>
          </v-toolbar>
          <v-toolbar color="rgba(0, 0, 0, 0)" class="mt-n8">
            <h4 class="" >6,50%</h4>
            <span class="caption text-grey" >+ 6,7%</span>
          </v-toolbar>
          <v-toolbar color="rgba(0, 0, 0, 0)" class="mt-n12">
            <v-progress-linear color="orange" height="6" model-value="6" stream>
            </v-progress-linear>
          </v-toolbar>
          <v-card-text class="pt-0 mt-n5 text-center ">
            <span class="text-caption text-grey">Yearly Goal</span>
          </v-card-text>
        </v-card>
      </v-col>

      <v-col cols="12" sm="4" class="pa-10">
        <v-card color="#242426" class="rounded-lg mx-2 pa-5">
          <v-toolbar color="rgba(0, 0, 0, 0)" class="mt-n7">
            <span class="caption text-grey" >Sales</span>
          </v-toolbar>
          <v-toolbar color="rgba(0, 0, 0, 0)" class="mt-n8">
            <h4 class="" >96,50%</h4>
            <span class="caption text-grey" >+ 6,7%</span>
          </v-toolbar>
          <v-toolbar color="rgba(0, 0, 0, 0)" class="mt-n12">
            <v-progress-linear color="orange" height="6" model-value="96" stream>
            </v-progress-linear>
          </v-toolbar>
          <v-card-text class="pt-0 mt-n5 text-center ">
            <span class="text-caption text-grey">Yearly Goal</span>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

  </v-card>
</template>

<script setup>

</script>

<style lang="scss">

</style>
