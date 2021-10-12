<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="12">
          <v-card class="mb-3 pb-4" elevation="0">
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
      <carousel/>
      <v-card class="pa-4 mt-6" elevation="2">
        <div class="headline mb-8">Assignments & Events 36</div>
        <Tabs/>
        
      </v-card>
    </v-col>
    
  </v-row>
  
</template>
<script>
import carousel from "~/components/home/Carousel.vue";
import Tabs from "~/components/home/Tabs.vue";
export default {
  components:{
    carousel,
    Tabs
  
  },
      data: () => ({
      items: [
        {
          text: 'Dashboard',
          disabled: false,
          href: '/',
        },
       
      ],
    }),
}
</script>
<style scoped>
.card-container{
  border-bottom: 4px solid #A2B6C8;
}
.card-link{
 text-decoration: none;
}
</style>