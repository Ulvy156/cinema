<template>
  <section class="w-[70%] m-auto my-8">
    <div class="flex gap-x-10 items-center">
      <h1 class="text-3xl text-white">Now Showing</h1>
      <span class="border-r h-6 border-gray-300"></span>
      <h1 class="text-3xl text-gray-400">Coming Soon</h1>
    </div>
    <div class="flex items-center gap-x-5 mt-10">
      <div
        v-for="(date, index) in dateList"
        :key="date.year + date.month + date.day"
        :class="index === 0 ? 'border-[#bd0404]' : 'border-gray-600'"
        class="px-16 py-2 border-2 rounded-md bg-[#171717] flex flex-col items-center"
      >
        <p class="text-gray-300">{{ date.day }}</p>
        <p class="text-2xl text-white">{{ date.month }}</p>
        <p class="text-gray-300">{{ date.year }}</p>
      </div>
    </div>
    <!-- cards -->
    <div class="grid grid-cols-4 gap-5">
      <article v-for="(card, index) in cardImgList" :key="index" class="mt-10">
        <img :src="card.imgSrc" alt="" class="h-[50vh] rounded-md" />
        <p class="text-gray-400 my-2">{{ card.date }}</p>
        <p class="text-white">{{ card.title }}</p>
      </article>
    </div>
    <!-- what's new -->
     <div>
      <h1 class="text-4xl text-white mt-10">What's New?</h1>
       <el-carousel :interval="5000" arrow="always">
         <el-carousel-item v-for="item in newDataList" :key="item.title">
           <article
             v-for="item in newDataList"
             :key="item.title"
             class="mt-10 h-[50vh] bg-cover bg-center flex items-center"
             :style="{ backgroundImage: `url(${item.imgSrc})`, borderRadius: '10px' }"
           >
             <div class="text-white flex flex-col items-center justify-center gap-5 pl-10 h-full ">
               <h1 class="text-3xl">{{item.title}}</h1>
               <p class="text-gray-300">{{item.description}}</p>
               <button class="bg-white rounded-full py-3 px-6 text-[red]">Learn More</button>
             </div>
           </article>
         </el-carousel-item>
       </el-carousel>
     </div>
  </section>
</template>

<script lang="ts" setup>
const dateList = [
  {
    day: '29',
    month: 'May',
    year: '2025',
  },
  {
    day: '30',
    month: 'May',
    year: '2025',
  },
  {
    day: '31',
    month: 'May',
    year: '2025',
  },
  {
    day: '1',
    month: 'June',
    year: '2025',
  },
  {
    day: '2',
    month: 'June',
    year: '2025',
  },
]
const cardImgList = [
  {
    date: '29 May 2025',
    imgSrc: 'https://tickets.legend.com.kh/CDN/media/entity/get/Movies/HO00001899',
    title: 'Bring Her Back',
  },
  {
    date: '30 May 2025',
    imgSrc: 'https://tickets.legend.com.kh/CDN/media/entity/get/Movies/HO00001898',
    title: 'The Lost City',
  },
  {
    date: '31 May 2025',
    imgSrc: 'https://tickets.legend.com.kh/CDN/media/entity/get/Movies/HO00001897',
    title: 'The Great Adventure',
  },
  {
    date: '1 June 2025',
    imgSrc: 'https://tickets.legend.com.kh/CDN/media/entity/get/Movies/HO00001896',
    title: 'Mystery of the Ocean',
  },
  {
    date: '2 June 2025',
    imgSrc: 'https://tickets.legend.com.kh/CDN/media/entity/get/Movies/HO00001895',
    title: 'Journey to the Stars',
  },
  {
    date: '4 June 2025',
    imgSrc: 'https://tickets.legend.com.kh/CDN/media/entity/get/Movies/HO00001851',
    title: 'The Time Traveler',
  },
  {
    date: '3 June 2025',
    imgSrc: 'https://tickets.legend.com.kh/CDN/media/entity/get/Movies/HO00001894',
    title: 'The Secret of the Forest',
  },
]
const newDataList = [
  {
    title: 'New Movie Release',
    description: 'Check out the latest movie that just hit the theaters.',
    imgSrc:
      'https://coolbeans.sgp1.digitaloceanspaces.com/legend-cinema-prod/5bb25e91-4c54-4dc4-acbb-a1c6f7474c9d.jpeg',
  },
  {
    title: 'Special Screening Event',
    description: 'Join us for a special screening of a classic film.',
    imgSrc:
      'https://coolbeans.sgp1.digitaloceanspaces.com/legend-cinema-prod/5bb25e91-4c54-4dc4-acbb-a1c6f7474c9d.jpeg',
  },
]
</script>


<style scoped>
.bg-color {
  background: linear-gradient(to right, #363636 0%, black 100%);
}
</style>
