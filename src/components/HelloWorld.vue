<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <v-flex xs12>
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <h1 class="display-2 font-weight-bold mb-3">
          Velkommen til Bourbons
        </h1>
        <p class="subheading font-weight-regular">
          Her kan du finde priser og andre oplysninger om din yndlings bourbon, og måske finde en ny favorit.
<!--           <br>please join our online
          <a href="https://community.vuetifyjs.com" target="_blank">Discord Community</a> -->
        </p>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">Find din Bourbon</h2>

<!--         <v-layout justify-center>
          <a
            v-for="(next, i) in whatsNext"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-layout> -->
      </v-flex>
      <v-flex
      mb-5
      xs-12
      >

  <v-autocomplete
v-model="select"
:items="states"
:loading="isLoading"
:search-input.sync="search"
color="white"
hide-no-data
hide-selected
item-text="Description"
item-value="state"
placeholder="Find din Bourbon"
prepend-icon="mdi-magnify"
return-object
>
  </v-autocomplete>

      </v-flex>

 

    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
   
  }),
};
</script>
