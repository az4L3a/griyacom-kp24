<template>
  <section id="services" class="container">
    <h2>Our Services</h2>
    <div class="grid">
      <div class="card" v-for="service in services" :key="service.title">
        <div class="card-image" :style="{ backgroundImage: `url('${service.image}')` }"></div>
        <div class="card-content">
          <h3>{{ service.title }}</h3>
          <p>{{ service.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ServicesSection',
  data() {
    return {
      services: [
        {
          title: 'Computer Repair',
          description: 'Our expert technicians can diagnose and fix a wide range of computer issues, from hardware failures to software problems.',
          image: 'data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="400" height="200" viewBox="0 0 400 200"><rect width="400" height="200" fill="%23003b5c"/><text x="50%" y="50%" font-family="Arial" font-size="24" fill="%23ffffff" text-anchor="middle" dominant-baseline="middle">Computer Repair Image</text></svg>'
        },
        {
          title: 'Laptop Maintenance',
          description: 'Keep your laptop running at peak performance with our comprehensive maintenance services, including cleaning and optimizing.',
          image: 'data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="400" height="200" viewBox="0 0 400 200"><rect width="400" height="200" fill="%23003b5c"/><text x="50%" y="50%" font-family="Arial" font-size="24" fill="%23ffffff" text-anchor="middle" dominant-baseline="middle">Laptop Maintenance Image</text></svg>'
        },
        {
          title: 'Data Recovery',
          description: 'Lost important files? Our data recovery experts can help retrieve your valuable data from damaged or corrupted storage devices.',
          image: 'data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="400" height="200" viewBox="0 0 400 200"><rect width="400" height="200" fill="%23003b5c"/><text x="50%" y="50%" font-family="Arial" font-size="24" fill="%23ffffff" text-anchor="middle" dominant-baseline="middle">Data Recovery Image</text></svg>'
        }
      ]
    }
  }
}
</script>