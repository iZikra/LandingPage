<template>
  <div id="app">
    <Navbar />
    <Carousel />
    <div class="container my-5">
      <h2 class="text-center mb-4">Produk Unggulan</h2>
      <div class="row">
        <div class="col-md-4" v-for="(product, index) in products" :key="index">
          <Card :image="product.image" :title="product.title" :description="product.description" />
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Card,
    Footer
  },
  data() {
    return {
      products: [
        {
          image: 'https://via.placeholder.com/400x300',
          title: 'Produk 1',
          description: 'Deskripsi singkat produk 1.'
        },
        {
          image: 'https://via.placeholder.com/400x300',
          title: 'Produk 2',
          description: 'Deskripsi singkat produk 2.'
        },
        {
          image: 'https://via.placeholder.com/400x300',
          title: 'Produk 3',
          description: 'Deskripsi singkat produk 3.'
        }
      ]
    };
  }
};
</script>

<style>
@import url('https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css');

body {
  font-family: Arial, sans-serif;
}

footer {
  background-color: #343a40;
}
</style>
