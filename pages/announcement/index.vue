<template>
<div>
        <v-card class="mb-3 pb-3" elevation="0">
        <div class="card-container px-1 rounded-0 d-flex justify-space-between">
          <v-breadcrumbs :items="items" divider="/" large></v-breadcrumbs>
          <a
            class="card-link mt-4 me-2"
            href="https://africaeducationnetwork.s3.us-east-2.amazonaws.com/Manuals/AEN+USER+GUIDE+ORIGINAL1.pdf"
            target="_blank"
            rel="noopener noreferrer"
            >Help</a
          >
        </div>
      </v-card>
  <v-card class="pa-2" flat>
    <v-card-title>
      Announcement
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="mdi-magnify"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>
    <v-data-table
      :headers="headers"
      :items="worksite"
      :search="search"
    ></v-data-table>
  </v-card>
</div>
</template>
<script>
  export default {
    data () {
      return {
            items: [
      {
        text: "Dashboard",
        disabled: false,
        href: "/",
      },
      {
        text: "Announcement",
        disabled: true,
        href: "breadcrumbs_link_2",
      },
    ],
          search:"",
        headers: [
          {
            text: 'Worksite Title',
            align: 'justify',
            sortable: false,
            value: 'name',
          },
          { text: 'Type', align: 'justify', value: 'type' },
          { text: ' Creator', align: 'justify', value: 'creator' },
          { text: 'Term',align: 'justify',  value: 'term' },
          { text: 'Status',align: 'justify',  value: 'status' },
          { text: 'Creation Date', align: 'justify', value: 'creation' },
          { text: 'Action', align: 'justify', value: 'action' },
        ],
        worksite: [
          {
            name: 'writting ',
            type: 'Unofficial Lecture',
            creator: 'lamourette, prof ',
            term:'summer',
            status: 'open',
            creation: 'Monday, April 27th 2020',
            action: '',
          },
         
          {
            name: 'mathematic ',
            type: 'Unofficial Lecture',
            creator: 'No staff assigned yet  ',
            term:'Semestre 2',
            status: 'open',
            creation: 'Monday, April 27th 2020',
            action: '',
          },
         
          {
            name: 'belnew ',
            type: 'Unofficial Lecture',
            creator: 'ekaniProf, eternel  ',
            term:'Semestre 2',
            status: 'open',
            creation: 'Monday, April 27th 2020',
            action: '',
          },
         
          {
            name: 'chemistry mont  ',
            type: 'Unofficial Lecture',
             creator: 'ekaniProf, eternel  ',
            term:'summer',
            status: 'open',
            creation: 'Monday, April 27th 2020',
            action: '',
          },
         
        ],
      }
    },
  }
</script>