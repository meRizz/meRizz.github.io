<template>
  <v-item-group mandatory class="mt-n1">
    <v-container>
        <v-row justify="center" class="space">
            <v-col cols="12" xs="12" sm="4" md="2" v-for="(category, i) in categories" :key="i">
                <v-item v-slot="{ active, toggle }">
                    <v-card :color="active ? '#D5F0DB' : 'white'"
                    :class="active ? 'borderme' : 'borderout'"
                    class="d-flex align-center rounded-lg mx-2" dark height="180" flat @click="toggle">
                    <v-row>
                        <v-col cols="12" sm="12">
                            <v-list-item three-line class="text-center">
                                <v-list-item-content>
                                    <div align-center="center" justify="center" text-sm-center>
                                        <v-img :src="category.img" max-height="90" max-width="90" contain></v-img>
                                    </div>
                                    <v-list-item-subtitle
                                    :class="active ? 'green--text' : 'black--text'"
                                    class="caption mt-4"
                                    >
                                    {{ category.title }}
                                </v-list-item-subtitle>
                                    
                                </v-list-item-content>
                            </v-list-item>
                        </v-col>
                    </v-row>
                </v-card>
                </v-item>
            </v-col>
        </v-row>
    </v-container>
  </v-item-group>
</template>

<script>
export default {
  data: () => ({
    categories: [
      { img: "cat1.png", title: "Western Food" },
      { img: "cat2.png", title: "Indonesian Food" },
      { img: "cat3.png", title: "Korean Food" },
      { img: "cat4.png", title: "Dessert" },
      { img: "cat5.png", title: "Drink" },
    ],
  }),
};
</script>

<style>

</style>