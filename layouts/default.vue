<template>
  <v-app>
   
    <v-navigation-drawer
      v-model="drawer"
      :clipped="clipped"
      fixed
      app
      class="mt-12"
    >
      <v-list class="py-12">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
        <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
        </v-list-item>
        <v-list-item>
      <v-list-item-content>
        <v-list-item-title>
          <a href="https://africaeducationnetwork.s3.us-east-2.amazonaws.com/Manuals/AEN+USER+GUIDE+ORIGINAL1.pdf" class="card-link " target="_blank" rel="noopener noreferrer">Help</a>
        </v-list-item-title>
      </v-list-item-content>
       <v-list-item-action>
             <v-icon>mdi-help-circle</v-icon>
          </v-list-item-action>
    </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      color="#fff"
    >
      <v-toolbar-title>
 <div class="headline">Kelden Bilingual <span class="green--text text--accent-4">Institute </span></div>
      </v-toolbar-title>
      <v-spacer />
  <div class="bo text-body-2 font-italic font-weight-thin">Enter To Learn Leave To Achieve</div>
    </v-app-bar>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      color="#1564A3"
      class="mt-12"
    >
      <v-app-bar-nav-icon class="white--text" @click.stop="drawer = !drawer" />
      <v-toolbar-title class=" yellow--text" v-text="title" />
      <v-spacer />
 
    </v-app-bar>
    <v-main class="main">
      <v-container class="mt-12">
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: true,
      drawer: true,
      fixed: false,
      items: [
        {
          icon: 'mdi-home',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-flag',
          title: 'Anouncement',
          to: '/announcement'
        },
        {
          icon: 'mdi-calendar-cursor',
          title: 'Workside Setup',
          to: '/worksite'
        },
        {
          icon: 'mdi-calendar-blank',
          title: ' My Courses',
          to: '/courses'
        },
        {
          icon: 'mdi-account-supervisor',
          title: 'Membership',
          to: '/membership'
        },
        {
          icon: 'mdi-cog',
          title: 'Preferences',
          to: '/preferences'
        },
        {
          icon: 'mdi-account',
          title: 'Profile',
          to: '/profile'
        },
        {
          icon: 'mdi-book',
          title: 'Textbooks',
          to: '/textbook'
        },
        {
          icon: 'mdi-text-box-search',
          title: 'Library Search',
          to: '/library'
        },
        {
          icon: 'mdi-file',
          title: 'Schedule',
          to: '/shedule'
        },
        {
          icon: 'mdi-file-document-edit',
          title: 'Exams Center',
          to: '/exams'
        },
      ],
      title: 'My Workspace'
    }
  }
}
</script>
<style scoped>
.main{
  background-color:#FAFAFA ;
}
.card-link {
  text-decoration: none;
  color: #1b1b1b;
}
</style>
