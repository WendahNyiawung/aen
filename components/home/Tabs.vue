<template>
  <div>
    <template>
      <v-tabs>
        <v-tab>UPCOMING</v-tab>
        <v-tab-item>
         <upcoming/>
        </v-tab-item>
        <v-tab>PAST</v-tab>
        <v-tab-item>
          <past />
        </v-tab-item>
      </v-tabs>
    </template>
  </div>
</template>
  
  </div>
</template>
<script>
import past from "~/components/home/Past.vue";
import upcoming from "~/components/home/Upcoming.vue";
export default {
  components: {
    past,
    upcoming
  },
  
};
</script>
<style lang="scss" scoped>
.card-link{
    background-color: #fff;
     border-bottom: 4px solid #A2B6C8;
}

.card-link:hover{
    background-color: #F6F6F6;
}
</style> 

