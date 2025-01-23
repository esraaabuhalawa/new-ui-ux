<template>
  <main>
    <div class="top-img">
      <img src="../assets/images/Vector1.png">
    </div>
    <Navbar />
    <Banner />
    <Services /> 
    <About />
    <Achievements />
   <portofolio />
    <PortofolioSlide />
    <Testmonials/>
    <Contact />
    
    <FooterItem />
  </main>
</template>
<script>
import Navbar from '@/components/Layout/Navbar.vue';
import FooterItem from '@/components/Layout/FooterItem.vue';
import Banner from '@/components/HomePage/banner.vue';
import Services from '@/components/HomePage/services.vue';
import About from '@/components/HomePage/About.vue';
import Contact from '@/components/HomePage/Contact.vue';
import Testmonials from '@/components/HomePage/Testmonials.vue';
import Portofolio from '@/components/HomePage/Portofolio.vue';
import Achievements from '@/components/HomePage/Achievements.vue';
import PortofolioSlide from '@/components/HomePage/PortofolioSlide.vue';
export default {
  components: {
    Achievements,
    PortofolioSlide ,
    Navbar,
    Banner,
    Services,
    About,
    Contact,
    Testmonials,
    Portofolio,
    FooterItem
  }
}
</script>
