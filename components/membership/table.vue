<template>
  <div>
    <v-card flat class="pa-5">
       <div class="d-flex justify-end">
            <v-btn color="primary">
                <nuxt-link to="/membership/joinable" class="table-link">Joinable Sites</nuxt-link>
            </v-btn>
       </div>
      <v-card-title class="mb-5">
       My Current Sites
        <v-spacer></v-spacer>
        <v-text-field
          v-model="search"
          append-icon="mdi-magnify"
          label="Search"
          single-line
          hide-details
        ></v-text-field>
      </v-card-title>
      <v-simple-table>
        <template v-slot:default>
          <thead>
            <tr>
              <th class="text-justify">Worksite Title</th>
              <th class="text-justify">Creator</th>
              <th class="text-justify">Description</th>
              <th class="text-justify">Creation Date</th>
              <th class="text-justify">Action</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="item in members" :key="item.name">
              <td class="text-justify">{{ item.name }}</td>
              <td class="text-justify">{{ item.creator }}</td>
              <td class="text-justify">
                {{ item.des }} <br />
                <div class="text-center">
                  <v-dialog v-model="dialog" width="500">
                    <template v-slot:activator="{ on, attrs }">
                      <v-btn depressed elevation="0" color="white" class="t text--accent-3  blue--text" v-bind="attrs" v-on="on">
                        (MORE)
                      </v-btn>
                    </template>

                    <v-card>
                      <v-card-title class="text-h5 grey lighten-2">
                       Description 
                      </v-card-title>

                      <v-card-text>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        sed do eiusmod tempor incididunt ut labore et dolore
                        magna aliqua. Ut enim ad minim veniam, quis nostrud
                        exercitation ullamco laboris nisi ut aliquip ex ea
                        commodo consequat. Duis aute irure dolor in
                        reprehenderit in voluptate velit esse cillum dolore eu
                        fugiat nulla pariatur. Excepteur sint occaecat cupidatat
                        non proident, sunt in culpa qui officia deserunt mollit
                        anim id est laborum.
                      </v-card-text>

                      <v-divider></v-divider>

                      <v-card-actions>
                        <v-spacer></v-spacer>
                        <v-btn color="primary" text @click="dialog = false">
                         Close
                        </v-btn>
                      </v-card-actions>
                    </v-card>
                  </v-dialog>
                </div>
              </td>
              <td class="text-justify">
                {{ item.date }}
              </td>
              <td class="text-justify">
                <v-btn color="error" small>UNJOIN</v-btn>
              </td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
    </v-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
        search:"",
      dialog: false,
      members: [
        {
          name: "Mathematics",
          creator: "lamourette, prof ",
          des: "co ordinate geometry in depth ",
          date: "Monday, April 27th 2020",
          action: " ",
        },
        {
          name: "Mathematics",
          creator: "lamourette, prof ",
          des: "writing for Teachers",
          date: "Monday, April 27th 2020",
          action: " ",
        },
        {
          name: "Mathematics",
          creator: "lamourette, prof ",
          des: "writing for Teachers",
          date: "Monday, April 27th 2020",
          action: " ",
        },
      ],
    };
  },
};
</script>
<style scoped>
.table-link {
  text-decoration: none;
  color: #fff;
}
</style>