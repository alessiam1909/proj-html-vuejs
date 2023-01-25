<script >
import AppHeader from './components/AppHeader.vue'
import AppContent1 from './components/AppContent1.vue'
import AppFooter from './components/AppFooter.vue'

export default{
  components: {
    AppHeader,
    AppContent1,
    AppFooter
  }, 
  data(){
    return{
      activeItem: 0,
      navList: [
        {
          name: "HOME",
          url: "#null",
          stato: true
        },
        {
          name: "ABOUT",
          url: "https://avada.theme-fusion.com/driving/about/",
          stato: false
        },
        {
          name: "PRICES",
          url: "https://avada.theme-fusion.com/driving/prices/",
          stato: false
        },
        {
          name: "COURSES",
          url: "#",
          new: true,
          dropdownMenu: ["Intensive", "Pass Plus", "Instructor"],
          isOpen: false,
          stato: false
        },
        {
          name: "LOCATIONS",
          url: "https://avada.theme-fusion.com/driving/locations/",
          stato: false
        },
        {
          name: "BLOG",
          url: "https://avada.theme-fusion.com/driving/blog/",
          stato: false
        }
      ]
    }
  }
}
</script>

<template>
<AppHeader :navList="navList"/>
<AppContent1/>
<AppFooter/>
</template>

<style lang="scss">
@use './styles/generals.scss' as *
</style>
