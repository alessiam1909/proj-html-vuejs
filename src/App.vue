<script >
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'

export default{
  components: {
    AppHeader,
    AppFooter
  }, 
  data(){
    return{
      navList: [
        {
          name: "HOME",
          url: "#null"
        },
        {
          name: "ABOUT",
          url: "https://avada.theme-fusion.com/driving/about/"
        },
        {
          name: "PRICES",
          url: "https://avada.theme-fusion.com/driving/prices/"
        },
        {
          name: "COURSES",
          url: "https://avada.theme-fusion.com/driving/courses/"
        },
        {
          name: "LOCATIONS",
          url: "https://avada.theme-fusion.com/driving/locations/"
        },
        {
          name: "BLOG",
          url: "https://avada.theme-fusion.com/driving/blog/"
        }
      ]
    }
  }
}
</script>

<template>
<AppHeader :navList="navList"/>
<AppFooter/>
</template>

<style lang="scss">
@use './styles/generals.scss' as *
</style>
