<template>
  <v-row class="mt-10 mb-5">
    <v-col
      cols="12"
      xs="12"
      sm="6"
      md="6"
      v-for="(client, i) in clients"
      :key="i"
    >
        <v-card class="elevation-16 mx-auto" width="300">
        <v-list subheader two-line>
            <v-img  
              max-height="300"
              max-width="300"
              contain
              :src="client.img"></v-img>
          <v-list-item>
          </v-list-item>
        </v-list>
        <v-card-text>
          
          {{ client.bio }}
        </v-card-text>
      </v-card>
     
    </v-col>
    
    
  </v-row>
</template>

<script>
export default {
  data: () => ({
    rating: 4.5,
  
    clients: [
      {
        img: "c1.png",
      },
      {
        img: "c2.png",
      },
      {
        img: "c3.png",
      },
      {
        img: "c4.png",
      },
    ],
  }),
};
</script>

<style>
</style>