<template>
  <v-card>
    <v-toolbar color="#1D97A7" light>
      Announcements
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-toolbar>

    <v-data-table :headers="headers" :items="students" :search="search">
      <template v-slot:item.firstName="{ item }">
        <nuxt-link :to="`/announcement/details/${item.id}`">
          <v-btn color="#1D97A7" text>{{ item.firstName }}</v-btn>
        </nuxt-link>
      </template>
      <!-- <template v-slot:item.actions="{ item }">
        <v-icon small class="mr-2" @click="editItem(item)"> mdi-pencil </v-icon>
        <v-icon small @click="deleteItem(item)"> mdi-delete </v-icon>
      </template> -->
    </v-data-table>
  </v-card>
</template>
<script>
export default {
  name: "StudentTable",
  props: {
    announcement: Array,
    headers: Array,
  },
  data() {
    return {
      search: ""
    };
  }
};
</script>