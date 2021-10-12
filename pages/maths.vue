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
      <v-card flat class="pa-2">
        <v-card elevation="1" class="pa-5">
          <v-card-title>
            Assignments & Events
            <v-spacer></v-spacer>
          </v-card-title>
          <v-row>
            <v-col>
              <v-tabs>
                <v-tab>UPCOMING</v-tab>
                <v-tab-item>
                  <div class="text text-justify grey--text mt-2">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
                    do eiusmod tempor incididunt ut labore et dolore magna
                    aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                    ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </div>
                </v-tab-item>
                <v-tab>PAST</v-tab>
                <v-tab-item>
                  <div class="text text-justify grey--text mt-2">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
                    do eiusmod tempor incididunt ut labore et dolore magna
                    aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                    ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </div>
                </v-tab-item>
              </v-tabs>
            </v-col>
          </v-row>
        </v-card>
        <v-card elevation="1" class="pa-5 mt-8">
          <v-card-title>
            Recent Activities
            <v-spacer></v-spacer>
          </v-card-title>
          <v-row>
            <v-col>
              <v-tabs>
                <v-tab>UPCOMING</v-tab>
                <v-tab-item>
                  <div class="text text-justify grey--text mt-2">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
                    do eiusmod tempor incididunt ut labore et dolore magna
                    aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                    ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </div>
                </v-tab-item>
                <v-tab>PAST</v-tab>
                <v-tab-item>
                  <div class="text text-justify grey--text mt-2">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
                    do eiusmod tempor incididunt ut labore et dolore magna
                    aliqua. Ut enim ad minim veniam, quis nostrud exercitation
                    ullamco laboris nisi ut aliquip ex ea commodo consequat.
                  </div>
                </v-tab-item>
              </v-tabs>
            </v-col>
          </v-row>
        </v-card>
      </v-card>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        text: "Dashboard",
        disabled: false,
        href: "/",
      },
      {
        text: "Course Name",
        disabled: true,
        href: "breadcrumbs_link_2",
      },
    ],
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
.card-link:hover {
  border-bottom: #7ba9ce 1px solid;
}
</style>
