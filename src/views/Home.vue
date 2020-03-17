<template>
  <div class="home">
    <!-- Header Section Begin -->
    <Header/>
    <!-- Header End -->

    <!-- Carousel Section Begin -->
    <BannerCarousel/>
    <!-- Carousel Section End -->

    <!-- Carousel Section Begin -->
    <ProductCarousel/>
    <!-- Carousel Section End -->

    <!-- InstaImage Section Begin -->
    <InstaImage/>
    <!-- InstaImage Section End -->

    <!-- PartnerLogo Section Begin -->
    <PartnerLogo/>
    <!-- PartnerLogo Section End -->

    <!-- Footer Section Begin -->
    <Footer />
    <!-- Footer Section End -->
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import BannerCarousel from '@/components/BannerCarousel.vue'
import ProductCarousel from '@/components/ProductCarousel.vue'
import InstaImage from '@/components/InstaImage.vue'
import PartnerLogo from '@/components/PartnerLogo.vue'
import Footer from '@/components/Footer.vue'


export default {
  name: 'Home',
  components: {
    Header,
    BannerCarousel,
    ProductCarousel,
    InstaImage,
    PartnerLogo,
    Footer
  }
}
</script>
