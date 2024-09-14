<template>
  <div>
    <h1>Image Carousel</h1>
    <div class="carousel">
      <img :src="images[currentImage]" alt="carousel image" class="carousel-image" />
      <div class="controls">
        <button @click="prevImage">Previous</button>
        <button @click="nextImage">Next</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        "https://via.placeholder.com/600x400?text=Image+1",
        "https://via.placeholder.com/600x400?text=Image+2",
        "https://via.placeholder.com/600x400?text=Image+3"
      ],
      currentImage: 0
    };
  },
  methods: {
    nextImage() {
      this.currentImage = (this.currentImage + 1) % this.images.length;
    },
    prevImage() {
      this.currentImage = (this.currentImage - 1 + this.images.length) % this.images.length;
    }
  }
};
</script>

<style scoped>
.carousel {
  text-align: center;
  margin-top: 20px;
}
.carousel-image {
  max-width: 600px;
  max-height: 400px;
  margin-bottom: 10px;
}
.controls {
  display: flex;
  justify-content: center;
  gap: 10px;
}
button {
  padding: 10px;
  background-color: #42b983;
  color: white;
  border: none;
  cursor: pointer;
}
button:hover {
  background-color: #35495e;
}
</style>
