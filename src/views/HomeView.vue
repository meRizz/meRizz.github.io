<template>
  <div>
    <v-app>
  <NavbarItemVue />
  <the-modal>
    <component :is="Navbar" />
  </the-modal>
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-card class="mx-auto rounded-xl" flat>
            <v-img src="cover.png" max-height="100%" max-width="100%" contain>
              <v-card-title class="top ml-10">
                <h2 class="tittle1">Order your</h2>
              </v-card-title>
              <v-card-title class="ml-10 mt-n8">
                <h2 class="tittle2">Daily Menu</h2>
              </v-card-title>
              <v-card-text class="ml-10">
                <h3 class="green--text">#Free Delivery</h3>
              </v-card-text>
              
                  <v-card-text class="ml-10">
                  <v-row>
                  <v-col cols="4">
                    <v-text-field label="Search your daily menu" 
                    class="d-none d-sm-none d-md-flex" 
                    filled solo prepend-inner-icon="mdi-magnify" flat background-color="" rounded outlined success
                    >
                    </v-text-field>
                  </v-col>
                  <v-col cols="2" class="marginLeft">
                    <v-btn 
                    color="green" rounded dark x-large class="py-7 d-none d-sm-none d-md-flex">search</v-btn>
                  </v-col>
                </v-row>
                </v-card-text>
                
            </v-img>
          </v-card>
          <v-toolbar flat color="transparent">
            <v-toolbar-title class="text-h6">Category</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn-toggle v-model="toggle_exclusive" group color="#49D9A0">
              <v-btn>
                <v-icon>mdi-chevron-left</v-icon>
              </v-btn>
              <v-btn>
                <v-icon>mdi-chevron-right</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-toolbar>

          <CategoryItemVue />
          <the-modal>
            <component :is="Category" />
          </the-modal>
          <v-toolbar flat color="transparent" class="mt-5">
            <v-toolbar-title class="text-h6">Popular Product</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn rounded color="green" dark class="px-8">See All</v-btn>
          </v-toolbar>

          <ProductItemVue />
          <the-modal>
            <component :is="Product" />
          </the-modal>
          <v-card flat color="#E2F2E5" class="rounded-xl mt-8">
            <v-toolbar flat color="transparent"  class="mb-4">
              <v-toolbar-title class="text-h6 mt-5">Popular Bundle Pack</v-toolbar-title>
            </v-toolbar>
            <PackItemVue />
          </v-card>
          <v-card flat color="#FAFAFA" class="mt-8 py-5 px-16">
            <div
              style="position: absolute; margin-left: auto; margin-right: auto; left: 0; right: 0; text-align: center;">
              <h3>What Our Clients Say</h3>
            </div>
          </v-card>
          <ClientItemVue />

        </v-col>
      </v-row>
  </v-container>
</v-app>
  </div>
</template>

<script>
import NavbarItemVue from '@/components/NavbarItem.vue';
import CategoryItemVue from '@/components/CategoryItem.vue';
import ProductItemVue from '@/components/ProductItem.vue';
import PackItemVue from '@/components/PackItem.vue';
import ClientItemVue from '@/components/ClientItem.vue';

export default{
  name: 'HomeView',
  data: () => ({
    toggle_exclusive: 1,
    }),

  components: {
    NavbarItemVue,
    CategoryItemVue,
    ProductItemVue,
    PackItemVue,
    ClientItemVue,
}
  
}
</script>
<style>
.marginleft {
  margin-left: -90px;
}
.mtop {
  margin-top: 100px;
}
.mbottom {
  margin-bottom: 100px;
}
.v-card.borderme {
  border: 2px solid green;
}
.v-card-borderout {
  border: 1px solid #d5f0db !important;
}
.v-btn:not(.v-btn--round).v-size--default.add {
  min-width: 0px !important;
}
.theme--light.v-sheet--outlined.mobile {
  border: 2px solid black !important;
}
@media only screen and (max-width: 600px) {
  h2.title1 {
    font-size: 15px;
  }
  h2.title2 {
    font-size: 15px;
  }
  .top {
    margin-top: 20px;
  }
}
@media only screen and (min-width: 600px) {
  .top {
    margin-top: 70px;
  }
}
@media only screen and (min-width : 760px) {
  .top {
    margin-top: 120px;
  }
}
</style>