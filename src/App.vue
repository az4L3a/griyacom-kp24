<template>
  <div id="app">
    <a href="#main-content" class="skip-link">Skip to main content</a>
    <app-header></app-header>

    <main id="main-content">
      <hero-section></hero-section>
      <services-section></services-section>
      <products-section></products-section>
      <about-section></about-section>
      <cta-section></cta-section>
      <contact-section></contact-section>
    </main>

    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import HeroSection from './components/HeroSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import ProductsSection from './components/ProductsSection.vue'
import AboutSection from './components/AboutSection.vue'
import CtaSection from './components/CtaSection.vue'
import ContactSection from './components/ContactSection.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    HeroSection,
    ServicesSection,
    ProductsSection,
    AboutSection,
    CtaSection,
    ContactSection,
    AppFooter
  },
  mounted() {
    this.setupScrollBehavior()
    this.setupHeaderScroll()
    this.setupCardAnimations()
  },
  methods: {
    setupScrollBehavior() {
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
          e.preventDefault()
          document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
          })
        })
      })
    },
    setupHeaderScroll() {
      window.addEventListener('scroll', () => {
        const header = document.querySelector('header')
        if (window.scrollY > 50) {
          header.classList.add('scrolled')
        } else {
          header.classList.remove('scrolled')
        }
      })
    },
    setupCardAnimations() {
      const cards = document.querySelectorAll('.card')
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.animation = 'fadeIn 1s ease-out forwards'
          }
        })
      }, { threshold: 0.1 })

      cards.forEach(card => {
        observer.observe(card)
      })
    }
  }
}
</script>

<style src="./assets/styles.css"></style>