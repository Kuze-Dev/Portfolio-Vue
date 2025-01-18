<template>
    <!-- ====== Blog Section Start -->
    <section class="relative  mt-10 text-gray-800  ">
      <!-- SVG background -->
      <div class="absolute inset-0 pointer-events-none">
        <svg
          class="w-full h-full"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 1440 320"
        >
          <path
            fill="#4f46e5"
            fill-opacity="0.5"
            d="M0,64L48,101.3C96,139,192,213,288,208C384,203,480,117,576,112C672,107,768,181,864,218.7C960,256,1056,256,1152,234.7C1248,213,1344,171,1392,149.3L1440,128L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
          ></path>
        </svg>
      </div>
  
      <div class="container mx-auto">
        <div class="text-center">
          <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4">
            Project Portfolio
          </h2>
          <div class="lg:w-[50%] xl:w-[50%] px-5 mx-auto" >
          <p class="text-base md:text-lg lg:text-xl text-justify  xl:text-xl text-[14px] ">
            My portfolio reflects my commitment to continuous learning and growth in Web Development. Each project is an opportunity for me to showcase my skills and expertise.
          </p>
        </div>
        </div>
  
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 gap-8 px-4 mt-12">
          <template v-for="(item, index) in blogItems" :key="index">
            <div class="border border-gray-200 dark:border-dark-3 wrounded-lg overflow-hidden transition-transform duration-300 transform hover:scale-105 bg-white shadow-lg"> <!-- Added background color and shadow to the card -->
              <div class="overflow-hidden ">
                <img :src="item.image" alt="image" class="w-full h-full object-cover object-center" />
              </div>
              <div class="p-6">
                <span class="block mb-2 text-xs font-semibold uppercase">{{ item.date }}</span>
                <h3 class="text-xl font-semibold mb-2">{{ item.title }}</h3>
                <p class="text-justify">{{ item.details }}</p>
                <p class="text-base mt-2">{{ item.tools }}</p>

                <!-- Modern Button with Icon -->
              
              </div>
            </div>
          </template>
        </div>
      </div>
      <footerComponent class="mt-8"/>
    </section>
    <!-- ====== Blog Section End -->
    
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import footerComponent from '@/components/footerComponent.vue';
  
  const blogItems = ref([
   
    {
      image: '../src/assets/warsmows.png', 
      title: 'Water Refilling Sales Monitoring Web System (Dynamic Web System)',
      details: 'The Water Refilling Sales Monitoring Web System helps manage sales, inventory, and customer transactions in a water refilling business. It provides real-time updates, tracks stock levels, and generates sales reports automatically. This system makes operations more efficient and ensures accurate monitoring of daily business activities.',
      tools:'Tech Stack Used: HTML,CSS,TAILWIND CSS,VUE.JS,NODE,EXPRESS & MYSQL',
      // buttonText: 'View Details',
      // buttonLink: '#',
      // date: 'Mar 15, 2023'
    },
    {
      image: 'https://miro.medium.com/v2/resize:fit:1400/0*tJVlXDl5iExYSAzE', 
      title: 'Responsive Design Principles',
      details: 'Focused on creating visually appealing and user-friendly websites, I apply responsive design principles to ensure seamless experiences across all devices. With a strong foundation in Tailwind CSS, I craft clean and efficient layouts that adapt beautifully to any screen size.',
      // buttonText: 'View Details',
      // // buttonLink: '#',
      // // date: 'Jan 05, 2023'
    },
  
    {
      image: '../src/assets/Static Website.png', 
      title: 'Static Website',
      details: 'Static Website is a development project showcasing a clean and responsive design, built with HTML and CSS. By leveraging CSS Media Queries, I ensured the website adapts beautifully to different screen sizes and devices. This project highlights my ability to create functional and visually appealing static websites with a focus on responsiveness.'
      // buttonText: 'View Details',
      // buttonLink: '#',
      // date: 'Mar 21, 2024'
    },
    {
  image: '../src/assets/portfolio1.png', // Adjust the path to the actual image location
  title: 'Portfolio-Vue.js',
  details: 'Portfolio-Vue.js is a project I developed using Vue.js, showcasing my skills in building responsive and dynamic web applications. Designed with responsive design principles, it ensures seamless usability and aesthetics across all devices. This portfolio highlights my expertise in modern web development, with clean layouts and efficient functionality.'
  // buttonText: 'View Details',
  // buttonLink: '#'
},

    {
      image: 'https://miro.medium.com/v2/resize:fit:2526/1*_L4PsCyrhhSIXSL0XsiYew.png', 
      title: 'Optimizing Website Performance',
      details: 'Learn strategies to optimize website performance for better speed and user engagement.',
      // buttonText: 'View Details',
      // buttonLink: '#',
      // date: 'March 31, 2024'
    },
    {
      image: 'https://miro.medium.com/v2/resize:fit:2526/1*_L4PsCyrhhSIXSL0XsiYew.png', 
      title: 'Optimizing Website Performance',
      details: 'Learn strategies to optimize website performance for better speed and user engagement.',
      // buttonText: 'View Details',
      // buttonLink: '#',
      // date: 'March 31, 2024'
    },
   
    
  ])
  </script>
  
  <style scoped>
  .transition-transform {
    transition-property: transform;
  }
  
  .hover\:scale-105:hover {
    transform: scale(1.05);
  }
  </style>