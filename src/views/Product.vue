<template>
  <div class="product">
    <!-- Header Section Begin -->
    <Header/>
    <!-- Header End -->
    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="breadcrumb-text product-more text-left">
                        <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
                        <span>Detail</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
        <div class="container">
            <div class="row">
                <div class="col-lg-12">
                    <div class="row">
                        <div class="col-lg-6">
                            <div class="product-pic-zoom">
                                <img class="product-big-img" :src="default_photo" alt="" />
                            </div>
                            <div class="product-thumbs">
                                <carousel :dots="false" :nav="false" :autoplay="true" :loop="true" class="product-thumbs-track ps-slider ">
                                    <div class="pt" data-imgbigurl="img/mickey1.jpg" @click="change_photo(thumbs[0])" :class="thumbs[0] == default_photo ? 'active' : ''">
                                        <img src="img/mickey1.jpg" alt="" />
                                    </div>

                                    <div class="pt" data-imgbigurl="img/mickey2.jpg" @click="change_photo(thumbs[1])"  :class="thumbs[1] == default_photo ? 'active' : ''">
                                        <img src="img/mickey2.jpg" alt="" />
                                    </div>

                                    <div class="pt" data-imgbigurl="img/mickey3.jpg"  @click="change_photo(thumbs[2])"  :class="thumbs[2] == default_photo ? 'active' : ''">
                                        <img src="img/mickey3.jpg" alt="" />
                                    </div>

                                    <div class="pt" data-imgbigurl="img/mickey4.jpg"  @click="change_photo(thumbs[3])"  :class="thumbs[3] == default_photo ? 'active' : ''">
                                        <img src="img/mickey4.jpg" alt="" />
                                    </div>
                                </carousel>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="product-details text-left">
                                <div class="pd-title">
                                    <span>oranges</span>
                                    <h3>Pure Pineapple</h3>
                                </div>
                                <div class="pd-desc">
                                    <p>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id accusantium! Autem.
                                    </p>
                                    <p>
                                        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur.
                                        Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
                                        Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                                        impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                                    </p>
                                    <h4>$495.00</h4>
                                </div>
                                <div class="quantity">
                                    <a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Product Shop Section End -->

    <RelatedProduct/>
    <!-- Footer Section Begin -->
    <Footer />
    <!-- Footer Section End -->
  </div>
</template>

<script>
// @ is an alias to /src
  import Header from '@/components/Header.vue'
  import Footer from '@/components/Footer.vue'
  import RelatedProduct from '@/components/RelatedProduct.vue'
  import carousel from 'vue-owl-carousel'

  export default {
    name: 'Product',
    components: {
      Header,
      Footer,
      RelatedProduct,
      carousel
    },
    data (){
      return {
        default_photo : "img/mickey1.jpg",
        thumbs : [
          "img/mickey1.jpg",
          "img/mickey2.jpg",
          "img/mickey3.jpg",
          "img/mickey4.jpg"
        ]
      }
    },
    methods : {
      change_photo (url){
        this.default_photo = url;
      }
    }
  }
</script>

<style scoped>
  .pt{
    margin-right :10px;
  }
</style>
