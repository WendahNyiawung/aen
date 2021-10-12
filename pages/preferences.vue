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
        <v-card-title class="mb-5">
          Preferences <span class="white--text">  you </span><span class="hea subtitle-1 text--accent-2 red--text">  you must save changes to take effect</span>
          <v-spacer></v-spacer>
           <v-btn color="primary">SAVE</v-btn>
        </v-card-title>
        <div class="d-flex justify-space-around mt-10">
            <div>My Workspace</div>
            <div>Active Sites (your drawer)</div>
        </div>
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
        text: "Preference",
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
</style>
