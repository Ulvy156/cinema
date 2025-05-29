<template>
  <el-carousel :interval="4000" height="auto"  type="card">
    <el-carousel-item style="height: 50vh" v-for="item in imgLists" :key="item">
      <img loading="lazy" :src="item" alt="cover image"  />
    </el-carousel-item>
  </el-carousel>
</template>

<script lang="ts" setup>
const imgLists = [
  'https://coolbeans.sgp1.digitaloceanspaces.com/legend-cinema-prod/c4d845c4-8144-4aff-8a05-7cee65183da3.jpeg',
  'https://coolbeans.sgp1.digitaloceanspaces.com/legend-cinema-prod/c54d48b6-9b4e-48c0-8082-e4b2085a890a.jpeg',
  'https://coolbeans.sgp1.digitaloceanspaces.com/legend-cinema-prod/5fc3097e-92d6-40a9-ad08-57da9cf79ece.jpeg',
  'https://coolbeans.sgp1.digitaloceanspaces.com/legend-cinema-prod/84fe69e2-26bf-44a5-89c6-d5b31ad603ad.jpeg',
  'https://coolbeans.sgp1.digitaloceanspaces.com/legend-cinema-prod/8ff67c16-1564-425a-a376-e8e6a4ff3622.jpeg'
]
</script>
