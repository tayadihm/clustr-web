<template>
    <div>
      <h2>Lokasi Perumahan</h2>
      <GoogleMap :latitude="-6.200000" :longitude="106.816666" />
    </div>
  </template>
  
  <script>
  import GoogleMap from "@/components/GoogleMap.vue";
  
  export default {
    name: "Home",
    components: {
      GoogleMap,
    },
  };
  </script>
  