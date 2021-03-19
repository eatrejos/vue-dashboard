<template>
    <!-- give the sidebar z-50 class so its higher than the navbar if you want to see the logo -->
    <!-- you will need to add a little "X" button next to the logo in order to close it though -->
    <div class="sx:w-3/4 md:w-1/3 lg:w-64 fixed md:top-0 md:left-0 h-screen lg:block bg-gray-100 border-r z-30" :class="sideBarOpen ? '' : 'hidden'" id="main-nav">

          <div class="w-full h-20  flex px-4 items-center mb-8">
            <svg class="" width="33" height="30" viewBox="0 0 33 30" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M13.9852 27.4376C14.1797 26.9367 14.2725 26.4021 14.258 25.865C14.2877 24.3764 14.6855 22.9184 15.416 21.621C16.1447 20.3258 17.1838 19.2321 18.44 18.438C18.9051 18.1885 19.3148 17.8473 19.6442 17.4349C19.9737 17.0225 20.216 16.5476 20.3566 16.0389C20.4972 15.5301 20.5331 14.9982 20.4622 14.4751C20.3913 13.9521 20.215 13.4489 19.944 12.996C19.582 12.391 19.061 11.895 18.44 11.565C18.084 11.318 17.742 11.052 17.416 10.767L16.599 9.967C15.1019 8.3932 14.2624 6.30708 14.252 4.135C14.2675 3.59777 14.1752 3.06288 13.9806 2.56188C13.786 2.06089 13.493 1.60395 13.119 1.218C12.7466 0.832488 12.3004 0.52595 11.807 0.316684C11.3135 0.107418 10.783 -0.000286365 10.247 5.71818e-07C9.71132 0.000756001 9.18124 0.108938 8.68811 0.318146C8.19497 0.527354 7.74881 0.833339 7.376 1.218C7.00262 1.60462 6.71011 2.06183 6.51556 2.56287C6.32102 3.06391 6.22836 3.59872 6.243 4.136C6.25174 4.83344 6.44384 5.5163 6.8 6.116C7.15494 6.71469 7.66169 7.20902 8.269 7.549C10.728 9.105 12.439 12.08 12.439 15.006C12.4329 17.1592 11.6094 19.2298 10.135 20.799L8.275 22.451C7.668 22.79 7.161 23.284 6.805 23.884C6.448 24.483 6.257 25.167 6.248 25.865C6.23271 26.4022 6.32507 26.9371 6.51965 27.438C6.71423 27.939 7.0071 28.396 7.381 28.782C7.75344 29.1674 8.19967 29.4739 8.6931 29.6832C9.18652 29.8924 9.71704 30.0002 10.253 30C10.7888 29.9994 11.3191 29.8913 11.8124 29.682C12.3057 29.4728 12.7521 29.1668 13.125 28.782C13.4982 28.3955 13.7906 27.9384 13.9852 27.4376Z" fill="#A5B4FC"/>
              <path d="M19.417 6.36C18.976 5.698 18.741 4.919 18.741 4.123C18.7417 3.05673 19.1641 2.034 19.916 1.278C20.5698 0.62024 21.4321 0.210504 22.355 0.119089C23.2779 0.0276751 24.2039 0.260281 24.974 0.777001C25.6337 1.2199 26.1473 1.84836 26.45 2.583C26.7527 3.31848 26.8318 4.12692 26.6772 4.9071C26.5226 5.68728 26.1413 6.40452 25.581 6.969C25.0224 7.53193 24.3087 7.91563 23.5311 8.07112C22.7535 8.22661 21.9471 8.14685 21.215 7.842C20.4822 7.53685 19.8564 7.02107 19.417 6.36Z" fill="#A5B4FC"/>
              <path d="M20.522 22.518C21.181 22.076 21.956 21.84 22.748 21.84V21.838C23.2745 21.8386 23.7957 21.9432 24.2816 22.1457C24.7676 22.3482 25.2088 22.6446 25.58 23.018C26.2359 23.6779 26.6439 24.544 26.735 25.47C26.8261 26.3959 26.5948 27.3249 26.08 28.1C25.6406 28.762 25.0144 29.2785 24.281 29.584C23.5489 29.8888 22.7426 29.9686 21.9649 29.8131C21.1873 29.6576 20.4736 29.2739 19.915 28.711C19.3545 28.1464 18.9731 27.429 18.8185 26.6486C18.6639 25.8683 18.743 25.0596 19.046 24.324C19.3488 23.5894 19.8624 22.9609 20.522 22.518Z" fill="#A5B4FC"/>
              <path d="M32.325 12.758C32.7648 13.4198 32.9998 14.1974 33 14.9931C32.9993 16.0597 32.577 17.0827 31.825 17.839C31.4537 18.2122 31.0125 18.5086 30.5265 18.7111C30.0406 18.9136 29.5195 19.0182 28.993 19.019C28.2001 19.019 27.4252 18.783 26.767 18.341C26.1073 17.8981 25.5937 17.2696 25.291 16.535C24.9881 15.7994 24.9089 14.9907 25.0635 14.2104C25.2181 13.43 25.5995 12.7126 26.16 12.148C26.7187 11.5849 27.4325 11.2011 28.2104 11.0456C28.9882 10.8901 29.7948 10.9699 30.527 11.275C31.2599 11.5804 31.8857 12.0966 32.325 12.758Z" fill="#A5B4FC"/>
              <path d="M1.781 11.647C2.44 11.205 3.214 10.969 4.007 10.969C4.53335 10.9701 5.05431 11.075 5.54008 11.2776C6.02585 11.4803 6.46691 11.7767 6.838 12.15C7.49361 12.8097 7.90142 13.6754 7.99252 14.601C8.08362 15.5265 7.85243 16.4552 7.338 17.23C6.89867 17.8914 6.27291 18.4075 5.54 18.713C4.80764 19.0164 4.00167 19.0953 3.22435 18.9399C2.44703 18.7845 1.7334 18.4017 1.174 17.84C0.613705 17.2755 0.232393 16.5583 0.0778156 15.7781C-0.0767617 14.9979 0.00226578 14.1895 0.305002 13.454C0.607595 12.719 1.12122 12.0902 1.781 11.647Z" fill="#A5B4FC"/>
            </svg>
            <p class="font-semibold text-2xl text-white pl-4">workflow</p>
          </div>
          <div class="mb-4 px-2">            
            <div :class="[{'route-link-active':path == '/dashboard/home'},'w-full flex items-center text-white h-10 p-4 pl-4 hover:bg-blue-800 rounded-lg cursor-pointer']">
              <svg width="20" height="20" class="mr-3" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1 10L3 8M3 8L10 1L17 8M3 8V18C3 18.5523 3.44772 19 4 19H7M17 8L19 10M17 8V18C17 18.5523 16.5523 19 16 19H13M7 19C7.55228 19 8 18.5523 8 18V14C8 13.4477 8.44772 13 9 13H11C11.5523 13 12 13.4477 12 14V18C12 18.5523 12.4477 19 13 19M7 19H13" stroke="#A5B4FC" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
              <router-link to="/dashboard" exact><span class="text-white">Dashboard</span></router-link>
            </div>
            <div :class="[{'route-link-active':path == '/dashboard/team'},'w-full flex items-center text-white h-10 p-4 pl-4 hover:bg-blue-800 rounded-lg cursor-pointer']">
              <svg class="mr-3" width="20" height="20" viewBox="0 0 20 20"  fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M10 2.35418C10.7329 1.52375 11.8053 1 13 1C15.2091 1 17 2.79086 17 5C17 7.20914 15.2091 9 13 9C11.8053 9 10.7329 8.47624 10 7.64582M13 19H1V18C1 14.6863 3.68629 12 7 12C10.3137 12 13 14.6863 13 18V19ZM13 19H19V18C19 14.6863 16.3137 12 13 12C11.9071 12 10.8825 12.2922 10 12.8027M11 5C11 7.20914 9.20914 9 7 9C4.79086 9 3 7.20914 3 5C3 2.79086 4.79086 1 7 1C9.20914 1 11 2.79086 11 5Z" stroke="#A5B4FC" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
              <router-link to="/dashboard/team" exact><span class="text-white">Team</span></router-link>
            </div>
            <div :class="[{'route-link-active':path == '/dashboard/'},'w-full flex items-center text-white h-10 p-4 pl-4 hover:bg-blue-800 rounded-lg cursor-pointer']">
              <svg width="20" class="mr-3" height="16" viewBox="0 0 20 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M1 3V13C1 14.1046 1.89543 15 3 15H17C18.1046 15 19 14.1046 19 13V5C19 3.89543 18.1046 3 17 3H11L9 1H3C1.89543 1 1 1.89543 1 3Z" stroke="#A5B4FC" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
              <span class="text-white">Projects</span>
            </div>
            <div :class="[{'route-link-active':path == '/dashboard/'},'w-full flex items-center text-white h-10 p-4 pl-4 hover:bg-blue-800 rounded-lg cursor-pointer']">
              <svg class="mr-3" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M6 5V1M14 5V1M5 9H15M3 19H17C18.1046 19 19 18.1046 19 17V5C19 3.89543 18.1046 3 17 3H3C1.89543 3 1 3.89543 1 5V17C1 18.1046 1.89543 19 3 19Z" stroke="#A5B4FC" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>

              <span class="text-white">Calendar</span>
            </div>
            <div :class="[{'route-link-active':path == '/dashboard/'},'w-full flex items-center text-white h-10 p-4 pl-4 hover:bg-blue-800 rounded-lg cursor-pointer']">
              <svg class="mr-3" width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M17 10V3C17 1.89543 16.1046 1 15 1H3C1.89543 1 1 1.89543 1 3V10M17 10V15C17 16.1046 16.1046 17 15 17H3C1.89543 17 1 16.1046 1 15V10M17 10H14.4142C14.149 10 13.8946 10.1054 13.7071 10.2929L11.2929 12.7071C11.1054 12.8946 10.851 13 10.5858 13H7.41421C7.149 13 6.89464 12.8946 6.70711 12.7071L4.29289 10.2929C4.10536 10.1054 3.851 10 3.58579 10H1" stroke="#A5B4FC" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>

              <span class="text-white">Documents</span>
            </div>
            <div :class="[{'route-link-active':path == '/dashboard/'},'w-full flex items-center text-white h-10 p-4 pl-4 hover:bg-blue-800 rounded-lg cursor-pointer']">
              <svg class="mr-3" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M7 17V11C7 9.89543 6.10457 9 5 9H3C1.89543 9 1 9.89543 1 11V17C1 18.1046 1.89543 19 3 19H5C6.10457 19 7 18.1046 7 17ZM7 17V7C7 5.89543 7.89543 5 9 5H11C12.1046 5 13 5.89543 13 7V17M7 17C7 18.1046 7.89543 19 9 19H11C12.1046 19 13 18.1046 13 17M13 17V3C13 1.89543 13.8954 1 15 1H17C18.1046 1 19 1.89543 19 3V17C19 18.1046 18.1046 19 17 19H15C13.8954 19 13 18.1046 13 17Z" stroke="#A5B4FC" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>

              <span class="text-white">Reports</span>
            </div>
          </div>


        </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
    name: 'Sidebar',
    computed: {
        ...mapState(['sideBarOpen']),
        path () {
          return this.$route.path;
        }
        
    }
}
</script>
<style >
#main-nav{
  background: #4338CA;
}
.route-link-active{
  background-color: #3730A3;
}
</style>