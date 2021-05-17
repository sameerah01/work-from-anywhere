<template>
    <v-app id="inspire">
    <v-app-bar app color="#16847e">
        <v-app-bar-nav-icon class="white--text"></v-app-bar-nav-icon>
        <v-toolbar-title class="white--text">Workaction</v-toolbar-title>
        <v-spacer></v-spacer>

        <v-btn class="ma-5 white--text" plain>
            Home
        </v-btn>

        <v-btn class="ma-5 white--text" plain>
            Book
        </v-btn>

        <v-btn class="ma-5 white--text" plain>
            Contact
        </v-btn>
    </v-app-bar>

    <v-carousel v-model="model" height="660px">
        <v-carousel-item v-for="color in colors" :key="color">
            <v-sheet tile>
            <v-row class="fill-height" align="center" justify="center">
                <v-img
                :src="require(`../assets/${color}.jpg`)"
                height="680px"
                width="1500px"
                >
                </v-img>
            </v-row>
            </v-sheet>
        </v-carousel-item>
        
    </v-carousel>
    
        <template>
  <v-container >
      <v-card color="#16847e" elevation="2">
          <v-row no-gutters class="ma-5 pa-5" >
      <v-col >
          <v-text-field
            class="mx-5 pt-5"
            label="Check In"
            solo
          ></v-text-field>

      </v-col>
      <v-col>
        
          <v-text-field
          class="mx-5 pt-5"
            label="Check Out"
            solo
          ></v-text-field>

      </v-col>
      <v-col class="pt-5">
          <v-btn
            height="45px"
            class="mx-5"
            dark
            solo
          >Check Availabality</v-btn>

      </v-col>
    </v-row>
      </v-card>
    
  </v-container>
</template>
   
    </v-app>
</template>

<script>
export default {
    data: () => ({
        model: 0,
        colors: ["pic10", "pic12", "pic13"],
    }),
};
</script>

<style scoped>
.abc {
    font-family: Raleway, sans-serif !important;
    font-size: 20px !important;
}

@media (min-width: 1500px){
    .container {
    max-width: 1200px;
}
}


</style>
