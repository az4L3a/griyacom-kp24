<template>
  <section id="products" class="container">
    <h2>Our Products</h2>
    <div class="grid">
      <div class="card" v-for="product in products" :key="product.title">
        <div class="card-image" :style="{ backgroundImage: `url('${product.image}')` }"></div>
        <div class="card-content">
          <h3>{{ product.title }}</h3>
          <p>{{ product.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import computerAccessoriesImage from '@/assets/computer-accessories-image.jpg'
import laptopComponentsImage from '@/assets/laptop-components-image.jpg'
import networkingEquipmentImage from '@/assets/networking-equipment-image.jpg'

export default {
  name: 'ProductsSection',
  data() {
    return {
      products: [
        {
          title: 'Aksesoris Komputer',
          description: 'Jelajahi berbagai aksesoris komputer berkualitas tinggi yang kami tawarkan, seperti keyboard, mouse, dan monitor.',
          image: computerAccessoriesImage
        },
        {
          title: 'Komponen Laptop',
          description: 'Tingkatkan kinerja laptop Anda dengan berbagai komponen yang tersedia, seperti RAM, SSD, dan baterai pengganti.',
          image: laptopComponentsImage
        },
        {
          title: 'Perangkat Jaringan',
          description: 'Tingkatkan jaringan rumah atau kantor Anda dengan pilihan router, switch, dan perangkat jaringan lainnya dari kami.',
          image: networkingEquipmentImage
        }
      ]
    }
  }
}
</script>
