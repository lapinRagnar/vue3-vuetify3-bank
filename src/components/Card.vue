<template>

  <v-card color="#242426" class="rounded-lg pb-1 mt-10">

    <v-toolbar color="transparent">
      <v-toolbar-title>Your Cards</v-toolbar-title>
    </v-toolbar>

    <v-card color="#242426" class="rounded-lg mx-2 pa-1 gradient flip">

      <v-toolbar variant="flat" color="transparent" >
        <v-toolbar-title class="text-grey text-caption">Universal Card</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-icon color="grey">fab fa-cc-mastercard</v-icon>
      </v-toolbar>

      <span class="text-grey text-caption ml-4">Balance</span>

      <h2 class="ml-4">4 799,56€</h2>

      <v-card-text class="pt-0 mt-4">
        <span class="font-weight-light">**** **** **** *542</span>
      </v-card-text>

      <v-toolbar variant="flat" color="transparent">
        <v-toolbar-title>Chats</v-toolbar-title>
        <v-chip color="green" class="ml-2">2</v-chip>
      </v-toolbar>

      <v-list color="transparent">

        <v-list-item
          v-for="(chat, i) in chats"
          :key="i"
          :title="chat.title"
          :subtitle="chat.subtitle"
        >

          <template v-slot:default>

            <v-avatar>
              <v-img :src="chat.img" ></v-img>
            </v-avatar>


            <v-list-item-action>
              <h5>{{ chat.date }}</h5>
              <v-btn>
                <v-icon color="grey">fas fa-chevron-right</v-icon>
              </v-btn>
            </v-list-item-action>

          </template>



        </v-list-item>
      </v-list>

      <v-card color="#242426" class="rounded-lg mx-2 pa-1 gradient mt-5">
        <h2 class="ml-4">Premium Kit</h2>
        <span class="text-grey mt-4 ml-4 text-caption">Get out about our new Item</span> <br>
        <span class="text-grey mt-4 ml-4 text-caption">For your love</span> <br>

        <v-card-text>
          <v-btn class="without-uppercase" color="#524eed">Oooooooooh Yes 100 €</v-btn>
        </v-card-text>
      </v-card>

    </v-card>

  </v-card>

</template>

<script setup>

  import { ref } from 'vue';


  const chats = ref([
    {
      img: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
      subtitle: "Allright then, see you later !",
      title: "Esther Howard",
      date: "12/06/2033",
    },
    {
      img: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
      subtitle: "Allright then, see you later ! ",
      title: "Floyd Miles",
      date: "12/06/2053",
    },
    {
      img: "https://cdn.vuetifyjs.com/images/lists/4.jpg",
      subtitle: "Allright then, see you later ! ",
      title: "Brooklyn Simmons",
      date: "12/06/3003",
    },
  ])

</script>

<style lang="scss">

  .gradient {
    background: rgb(63, 94, 251);
    background: radial-gradient(
      circle,
      rgba(63, 94, 251, 1) 0%,
      rgba(52, 36, 69, 1) 100%
    );
  }

  .flip {
    transform-style: preserve-3d;
    transition: all 0.8s ease;
  }

  .flip:hover {
    transform: rotateY(180deg);
  }

</style>
