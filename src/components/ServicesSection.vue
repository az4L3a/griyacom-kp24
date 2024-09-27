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
import computerRepairImage from '@/assets/computer-repair-image.jpg'
import laptopMaintenanceImage from '@/assets/laptop-maintenance-image.jpg'
import dataRecoveryImage from '@/assets/data-recovery-image.jpg'

export default {
  name: 'ServicesSection',
  data() {
    return {
      services: [
        {
          title: 'Perbaikan Komputer',
          description: 'Teknisi ahli kami dapat mendiagnosis dan memperbaiki berbagai masalah komputer, mulai dari kerusakan perangkat keras hingga permasalahan perangkat lunak.',
          image: computerRepairImage
        },
        {
          title: 'Perawatan Laptop',
          description: 'Jaga performa laptop Anda tetap optimal dengan layanan perawatan lengkap dari kami, termasuk pembersihan dan optimasi sistem.',
          image: laptopMaintenanceImage
        },
        {
          title: 'Pemulihan Data',
          description: 'Kehilangan data penting? Ahli pemulihan data kami siap membantu mengembalikan file Anda yang hilang dari perangkat penyimpanan yang rusak atau corrupt.',
          image: dataRecoveryImage
        }
      ]
    }
  }
}
</script>