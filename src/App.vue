<script >
import AppHeader from './components/AppHeader.vue'
import AppContent1 from './components/AppContent1.vue'
import AppContent2 from './components/AppContent2.vue'
import AppContent3 from './components/AppContent3.vue'
import AppContent4 from './components/AppContent4.vue'
import AppContent5 from './components/AppContent5.vue'
import AppContent6 from './components/AppContent6.vue'
import AppFooter from './components/AppFooter.vue'


export default{
  components: {
    AppHeader,
    AppContent1,
    AppContent2,
    AppContent3,
    AppContent4,
    AppContent5,
    AppContent6,
    AppFooter,

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
      ],

      footerList:[
          {
            title: "Pass Plus"
          },
          {
            title: "Intensive Course"
          },
          {
            title: "Automatic"
          },
          {
            title: "Instructor Training"
          },
      ]
    }
  }
}
</script>

<template>
<AppHeader :navList="navList"/>
<AppContent1/>
<AppContent2/>
<AppContent3/>
<AppContent4/>
<AppContent5/>
<AppContent6/>
<AppFooter :footerList="footerList"/>
</template>

<style lang="scss">
@use './styles/generals.scss' as *
</style>
