<template>
  <v-row>
    <v-col class="text-center">
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
      <v-card flat class="mt-4 pa-5">
      <v-row>
    <v-col>
      <v-sheet height="500">
        <v-calendar
          :now="today"
          :value="today"
          color="primary"
        >
          <template v-slot:day="{ past, date }">
            <v-row
              class="fill-height"
            >
              <template v-if="past && tracked[date]">
                <v-sheet
                  v-for="(percent, i) in tracked[date]"
                  :key="i"
                  :title="category[i]"
                
                  :width="`${percent}%`"
                  height="100%"
                  tile
                ></v-sheet>
              </template>
            </v-row>
          </template>
        </v-calendar>
      </v-sheet>
    </v-col>
  </v-row>
      </v-card>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        text: "Home",
        disabled: false,
        href: "/",
      },
      {
        text: "Schedule",
        disabled: true,
        href: "breadcrumbs_link_2",
      },
    ],
    today: '2019-01-10',
      tracked: {
        '2021-01-09': [23, 45, 10],
        '2021-01-08': [10],
        '2021-01-07': [0, 78, 5],
        '2021-01-06': [0, 0, 50],
        '2021-01-05': [0, 10, 23],
        '2021-01-04': [2, 90],
        '2021-01-03': [10, 32],
        '2021-01-02': [80, 10, 10],
        '2021-01-01': [20, 25, 10],
      },
      colors: ['#1867c0', '#fb8c00', '#000000'],
      category: ['Development', 'Meetings', 'Slacking'],
  }),
};
</script>
<style scoped>
.card-container {
  border-bottom: 4px solid #a2b6c8;
}
.card-link {
  text-decoration: none;
}
</style>
