<template>
  <div>
    <NavBar />
    <header class="masthead bg-primary text-white text-center">
      <div class="container d-flex align-items-center flex-column">
        <img class="masthead-avatar mb-5" src="@/assets/img/avataaars.svg" alt="..." />
        <h1 class="masthead-heading text-uppercase mb-0">Chhay Sophal</h1>
        <div class="divider-custom divider-light">
          <div class="divider-custom-line"></div>
          <div class="divider-custom-icon"><i class="fas fa-star"></i></div>
          <div class="divider-custom-line"></div>
        </div>
        <p class="masthead-subheading font-weight-light mb-0">Web Developer - Web Designer - API - Database</p>
      </div>
    </header>

    <section class="page-section portfolio" id="portfolio">
      <div class="container">
        <h2 class="page-section-heading text-center text-uppercase text-secondary mb-0">Portfolio</h2>
        <div class="divider-custom">
          <div class="divider-custom-line"></div>
          <div class="divider-custom-icon"><i class="fas fa-star"></i></div>
          <div class="divider-custom-line"></div>
        </div>
        <div class="row justify-content-center">
          <PortfolioItem v-for="item in portfolioItems" :key="item.id" :title="item.title" :imageSrc="item.imageSrc" :modalId="item.modalId" />
        </div>
      </div>
    </section>

    <section class="page-section bg-primary text-white mb-0" id="about">
      <div class="container">
        <h2 class="page-section-heading text-center text-uppercase text-white">About</h2>
        <div class="divider-custom divider-light">
          <div class="divider-custom-line"></div>
          <div class="divider-custom-icon"><i class="fas fa-star"></i></div>
          <div class="divider-custom-line"></div>
        </div>
        <div class="row">
          <div class="col-lg-4 ms-auto"><p class="lead">Freelancer is a free bootstrap theme created by Start Bootstrap. The download includes the complete source files including HTML, CSS, and JavaScript as well as optional SASS stylesheets for easy customization.</p></div>
          <div class="col-lg-4 me-auto"><p class="lead">You can create your own custom avatar for the masthead, change the icon in the dividers, and add your email address to the contact form to make it fully functional!</p></div>
        </div>
        <div class="text-center mt-4">
          <a class="btn btn-xl btn-outline-light" href="https://startbootstrap.com/theme/freelancer/">
            <i class="fas fa-download me-2"></i>
            Free Download!
          </a>
        </div>
      </div>
    </section>

    <Footer />
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue';
import PortfolioItem from '@/components/PortfolioItem.vue';
import Footer from '@/components/Footer.vue';

// Import CSS
import '@/assets/css/styles.css';

// Import JavaScript
import '@/assets/js/scripts.js';

// Import images using ES6 import statements
import cabinImage from '@/assets/img/portfolio/cabin.png';
import cakeImage from '@/assets/img/portfolio/cake.png';

export default {
  name: 'HomeView',
  components: {
    NavBar,
    PortfolioItem,
    Footer,
  },
  data() {
    return {
      portfolioItems: [
        { id: 1, title: 'Log Cabin', imageSrc: cabinImage, modalId: 'portfolioModal1' },
        { id: 2, title: 'Tasty Cake', imageSrc: cakeImage, modalId: 'portfolioModal2' },
        // Add more items here
      ],
    };
  },
};
</script>

<style scoped>
/* Add custom styles if needed */
</style>