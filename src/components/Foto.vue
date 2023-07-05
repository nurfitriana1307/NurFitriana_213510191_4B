<template>
    <div class="foto-container">
      <h2>Foto</h2>
      <div class="photo-gallery">
        <div v-for="(photo, index) in photos" :key="index" class="photo">
          <img :src="photo.imageUrl" :alt="photo.title">
          <div class="caption">
            <h3>{{ photo.title }}</h3>
            <p>{{ photo.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Foto',
    data() {
      return {
        photos: [
          {
            title: 'Sunset',
            description: 'Beautiful sunset over the ocean.',
            imageUrl: 'https://i.pinimg.com/originals/fb/d9/e1/fbd9e149dd4507461180c73c58903089.jpg'
          },
          {
            title: 'Mountains',
            description: 'Majestic mountains covered in snow.',
            imageUrl: 'https://2.bp.blogspot.com/-w3CWINUinVw/Ux0xRPXR55I/AAAAAAAAAO0/BIR_qBKem_I/s1600/Gunung+Merapi+Sleman+Yogyakarta+Jawa+Tengah.jpg'
          },
          {
            title: 'Flowers',
            description: 'Vibrant flowers in full bloom.',
            imageUrl: 'https://img.ev.mu/images/attractions/6678/960x640/529078.jpg'
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .foto-container {
    text-align: center;
  }
  
  .photo-gallery {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
  }
  
  .photo {
    position: relative;
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  }
  
  .photo img {
    width: 100%;
    height: auto;
  }
  
  .caption {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 10px;
    background-color: rgba(0, 0, 0, 0.6);
    color: #fff;
    text-align: left;
  }
  
  .caption h3 {
    font-size: 18px;
    margin-bottom: 5px;
  }
  
  .caption p {
    font-size: 14px;
    margin-bottom: 0;
  }
  h2{
    color:rgb(60, 195, 215);
  }
  </style>
  
  