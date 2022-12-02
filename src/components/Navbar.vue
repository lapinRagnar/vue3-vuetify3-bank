<template>
  <v-app-bar color="transparent">
    <div class="ml-8">
      <h4 class="text-white">Bonjour</h4> <br>
      <p class="text-grey caption mt-n7">Let's manage our save now!</p>
    </div>

    <v-spacer></v-spacer>

    <v-text-field
      label="Search what you want here..."
      variant="filled"
      bg-color="#1D1C21"
      prepend-inner-icon="mdi:mdi-magnify"
      class="ml-5 mt-6"
    >
    </v-text-field>

    <v-spacer></v-spacer>

    <v-btn>
      <v-icon color="#878A94" icon="far fa-envelope"></v-icon>
    </v-btn>

    <v-btn stacked>

      <v-badge
        bordered
        color="red"
        content="2"
      >
        <v-icon color="#878A94">far fa-bell</v-icon>
      </v-badge>

    </v-btn>


    <v-btn>

      <v-avatar
        size="30"
      >
        <v-img src="https://Cdn.vuetifyjs.com/images/lists/1.jpg" />

      </v-avatar>

      <div class="ml-1">
        <p class="text-green mr-10">lapinRagnar</p>
      </div>

    </v-btn>



  </v-app-bar>
</template>

<script setup>

</script>
