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
          BookLists 
          <v-spacer></v-spacer>
         
        </v-card-title>
        <v-card elevation="1" class="pa-8">
            <v-row>
                <v-col>
                    <nuxt-link to="" class="card-link   headline  float-left">Oliver twist</nuxt-link>
                    <div class="tex font-weight-bold mt-12 text-left">Format: </div>
                    <div class="text-left">Main Author: </div>
                    <div class="text-left">Published/Created: </div>
                    <div class="text-left">Link:  </div>
                </v-col>
                <v-col>
                  
                    <div class="mt-12 subtitle-1 text-left">Hard Copy </div>
                    <div class="text-left">Oscard Wilde </div>
                    <div class="text-left">2010</div>
                    <nuxt-link to="" class="card-link float-left">www.online.com </nuxt-link>
                </v-col>
                <v-col>
                   
                    <div class="tex font-weight-bold mt-12 text-left">Description  </div>
                    <div class="text-left">children's book by oscard wilde  </div>
                   
                </v-col>
            </v-row>
        </v-card>
        <v-card elevation="1" class="pa-8 mt-10">
            <v-row>
                <v-col>
                    <nuxt-link to="" class="card-link   headline  float-left">Principles </nuxt-link>
                    <div class="tex font-weight-bold mt-12 text-left">Format: </div>
                    <div class="text-left">Main Author: </div>
                    <div class="text-left">Published/Created: </div>
                    <div class="text-left">Link:  </div>
                </v-col>
                <v-col>
                  
                    <div class="mt-12 subtitle-1 text-left">Hard Copy </div>
                    <div class="text-left">Ray Dalio </div>
                    <div class="text-left">2017</div>
                    <nuxt-link to="" class="card-link float-left">www.online.com </nuxt-link>
                </v-col>
                <v-col>
                   
                    <div class="tex font-weight-bold mt-12 text-left">Description  </div>
                    <div class="text-left">book on financial freedom  </div>
                   
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
        text: "Home",
        disabled: false,
        href: "/",
      },
      {
        text: "TextBook",
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
.card-link:hover{
    border-bottom: #7ba9ce 1px solid;
}
</style>
