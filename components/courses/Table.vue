<template>
  <div>
    <v-card flat class="pa-5">
          <v-card-title class="mb-5">
      My Courses
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
          <th class="text-justify">
            Subject
          </th>
          <th class="text-justify">
            Course
          </th>
          <th class="text-justify">
            Section
          </th>
          <th class="text-justify">
            Site
          </th>
          <th class="text-justify">
            Instructor/Contact
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in desserts"
          :key="item.name"
        >
          <td class="text-justify">{{ item.name }}</td>
          <td class="text-justify">{{ item.course }}</td>
          <td class="text-justify">{{ item.section }}</td>
          <td class="text-justify">
            <nuxt-link to="/maths" class="table-link">{{ item.site }}</nuxt-link>
          </td>
          <td class="text-justify">{{ item.instructor }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
    </v-card>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        search:"",
        desserts: [
          {
            name: 'Mathematics',
            course: 2120,
            section: "01",
            site:"GO TO SITE",
            instructor:"ekaniProf, eternel (ekaniProf@yahoo.com) "
          },
          {
            name: 'belnew',
            course: "" ,
             section: "",
              site:"GO TO SITE",
             instructor:"ekaniProf, eternel (ekaniProf@yahoo.com) "
          },   
          {
            name: 'chemistry mont',
            course:"" ,
             section: "",
              site:"GO TO SITE",
             instructor:"ekaniProf, eternel (ekaniProf@yahoo.com) "
          },   
          {
            name: 'writting',
            course: "",
             section: "",
              site:"GO TO SITE",
             instructor:"ekaniProf, eternel (ekaniProf@yahoo.com) "
          },   
        ],
      }
    },
  }
</script>
<style scoped>
.table-link{
  text-decoration: none;
}
</style>