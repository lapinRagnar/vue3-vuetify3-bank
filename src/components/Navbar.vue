<template>
  <v-app-bar color="transparent">
    <div>
      <h4 class="text-white">Bonjour</h4> <br>
      <p class="text-grey caption mt-n7">Let's manage our save now!</p>
    </div>

    <v-text-field
      label="Search what you want here..."
      variant="filled"
      bg-color="#1D1C21"
      prepend-inner-icon="mdi:mdi-magnify"
      class="ml-5"
    >
    </v-text-field>

    <v-spacer></v-spacer>

    <v-btn>
      <v-icon color="#878A94" icon="far fa-envelope"></v-icon>
    </v-btn>

    <v-badge
      bordered
      color="red"
      content="2"
      class="mx-5"
    >
      <v-icon color="#878A94">far fa-bell</v-icon>
    </v-badge>


    <v-btn>
      <v-avatar
        size="30"
      >
        <v-img src="https://Cdn.vuetifyjs.com/images/lists/1.jpg" />
      </v-avatar>
    </v-btn>

    <div>
      <p class="text-green mr-10">lapinRagnar</p>
    </div>

  </v-app-bar>
</template>

<script setup>

</script>

<style lang="scss">

</style>
