<template>
  <div class="map-container">
    <div id="map" ref="map" style="width: 100%; height: 400px"></div>
  </div>
</template>

<script>
export default {
  mounted() {
    // eslint-disable-next-line no-undef
    const map = new google.maps.Map(this.$refs.map, {
      center: { lat: -6.2584884465878465, lng: 106.78151751544885 }, // Koordinat Kantor Virtus
      zoom: 15,
    });

    // eslint-disable-next-line no-undef
    const marker = new google.maps.Marker({
      position: { lat: -6.2584884465878465, lng: 106.78151751544885 }, // Koordinat Pin
      map: map,
      title: 'Kantor Virtus', // Nama lokasi
    });

    // eslint-disable-next-line no-undef
    const infoWindow = new google.maps.InfoWindow({
      content: `<h3>Kantor Virtus</h3>
      <p>Jl. Sultan Iskandar Muda No.09 9, RT.6/RW.9, Kby. Lama Sel., Kec. Kby. Lama, Kota Jakarta Selatan, Daerah Khusus Ibukota Jakarta 12240</p><br>
      <a href="https://www.google.com/maps/place/Kantor+virtus/@-6.2584883,106.7789144,17z"
            target="_blank"
            rel="noopener noreferrer">
            <b>Buka di Google Maps</b>
        </a>`
      ,
    });

    marker.addListener('click', () => {
      infoWindow.open(map, marker);
    });
  },
};
</script>

<style scoped>
.map-container {
  margin: 20px 0;
  border: 2px solid #ccc;
  border-radius: 8px;
  overflow: hidden;
}
</style>
