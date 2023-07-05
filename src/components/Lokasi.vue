<template>
  <div class="lokasi-container">
    <h2>Lokasi</h2>
    <div class="map-container">
      <img :src="mapData.imageUrl" :alt="mapData.name">
      <div class="location-info">
        <h3>{{ mapData.name }}</h3>
        <p>{{ mapData.address }}</p>
        <br>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Lokasi',
  data() {
    return {
      mapData: {
        name: '',
        address: '',
        imageUrl: ''
      }
    };
  },
  mounted() {
    // Simulasi data lokasi
    this.mapData.name = 'Universitas Islam Riau (UIR)';
    this.mapData.address = ' Jalan Kaharuddin Nasution, Simpang Tiga, Kota Pekanbaru, Riau, Indonesia';
    this.mapData.imageUrl = 'http://pmb.uir.ac.id/assets/img/map.jpg';
  }
};
</script>

<style scoped>
.lokasi-container {
  text-align: center;
}

.map-container {
  position: relative;
  display: inline-block;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.map-container img {
  width: 350px;
  height: auto;
}

.location-info {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  padding: 0px;
  background-color: rgba(0, 0, 0, 0.6);
  color: #fff;
  text-align: left;
}

.location-info h3 {
  font-size: 18px;
  margin-bottom: 10px;
}

.location-info p {
  font-size: 14px;
  margin-bottom: 0;
}
h2{
  color:rgb(162, 0, 255);
}
</style>

