<template>
  <!-- <div>
    <TheHeader />
    <Sidenav />
    <Nuxt />
    <TheFooter />
  </div> -->



  
  <v-app>
    <AppBarComponent />
    <!-- Sizes your content based upon application components -->
    <v-main class="ma-0 pa-0">
      <main class="ma-0 pa-0" ></main>
      <!-- Provides the application the proper gutter -->
      <v-container class="ma-0 pa-0" fluid  >
        <Nuxt  />
        <!-- If using vue-router -->
      </v-container>
    </v-main>
   
  </v-app>
</template>