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
export default {
  name: 'ProductsSection',
  data() {
    return {
      products: [
        {
          title: 'Computer Accessories',
          description: 'Browse our selection of high-quality computer accessories, including keyboards, mice, and monitors.',
          image: 'data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="400" height="200" viewBox="0 0 400 200"><rect width="400" height="200" fill="%23003b5c"/><text x="50%" y="50%" font-family="Arial" font-size="24" fill="%23ffffff" text-anchor="middle" dominant-baseline="middle">Computer Accessories Image</text></svg>'
        },
        {
          title: 'Laptop Components',
          description: 'Upgrade your laptop with our range of components, such as RAM, SSDs, and replacement batteries.',
          image: 'data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="400" height="200" viewBox="0 0 400 200"><rect width="400" height="200" fill="%23003b5c"/><text x="50%" y="50%" font-family="Arial" font-size="24" fill="%23ffffff" text-anchor="middle" dominant-baseline="middle">Laptop Components Image</text></svg>'
        },
        {
          title: 'Networking Equipment',
          description: 'Improve your home or office network with our selection of routers, switches, and other networking gear.',
          image: 'data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="400" height="200" viewBox="0 0 400 200"><rect width="400" height="200" fill="%23003b5c"/><text x="50%" y="50%" font-family="Arial" font-size="24" fill="%23ffffff" text-anchor="middle" dominant-baseline="middle">Networking Equipment Image</text></svg>'
        }
      ]
    }
  }
}
</script>