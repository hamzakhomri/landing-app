<template>
  <!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Motori-Style Store</title>

  <!--
    - favicon
  -->
  <link rel="shortcut icon" href="./assets/images/logo/logo_white.ico" type="image/x-icon">

  <!--
    - custom css link
  -->
  <link rel="stylesheet" href="./assets/css/style-prefix.css">

  <!--
    - google font link
  -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap"
    rel="stylesheet">

</head>

<body>


  <div :class="{ 'active': isOverlayActive }" @click="closeMobileMenus" class="overlay" data-overlay></div>

  <!--- MODAL   -->

  <!-- <div class="modal" :class="{ 'closed': isModalClosed }"  data-modal>

    <div class="modal-close-overlay" data-modal-overlay></div>

    <div class="modal-content">

      <button @click="closeModal" class="modal-close-btn" data-modal-close>
        <ion-icon name="close-outline"></ion-icon>
      </button>

      <div class="newsletter-img">
        <img src="./assets/images/newsletter.png" alt="subscribe newsletter" width="400" height="400">
      </div>

      <div class="newsletter">

        <form action="#">

          <div class="newsletter-header">

            <h3 class="newsletter-title">Subscribe Newsletter.</h3>
      

            <p class="newsletter-desc">
              Subscribe the <b>Anon</b> to get latest products and discount update.
            </p>

          </div>

          <input type="email" name="email" class="email-field" placeholder="Email Address" required>

          <button type="submit" class="btn-newsletter">Subscribe</button>

        </form>

      </div>

    </div>

  </div> -->

  <!---    NOTIFICATION TOAST   -->

  <div :class="{ 'closed': isToastClosed }" class="notification-toast" data-toast>

    <button  @click="closeToast" class="toast-close-btn" data-toast-close>
      <ion-icon name="close-outline"></ion-icon>
    </button>

    <div class="toast-banner">
      <img src="./assets/images/products/jewellery-1.jpg" alt="Rose Gold Earrings" width="80" height="70">
    </div>

    <div class="toast-detail">

      <p class="toast-message">
        Someone in new just bought
      </p>

      <p class="toast-title">
        Rose Gold Earrings
      </p>

      <p class="toast-meta">
        <time datetime="PT2M">2 Minutes</time> ago
      </p>

    </div>

  </div>





  <!--
    - HEADER
  -->

  <header>
      <HeaderComponent /> <!-- Use the updated component name here -->
    </header>






  <!--
    - MAIN
  -->

  <main>
    <BannerComponent />
    <BannerCategoryComponent />

    <div class="product-container">

      <div class="container">
        <!-- - SIDEBAR -->
        <div class="sidebar  has-scrollbar" data-mobile-menu>

          <SideBarCategoryComponents />
          <SideBarProductShowCase />
        </div>

        <div class="product-box">

          <ProductMinimal />
          <ProductFeatured />
          <ProductMain />

        </div>

      </div>

    </div>

    <div>
      <ContainerComponent />
    </div>

    <BlogComponent />
   

  </main>





  <!--
    - FOOTER
  -->

 <FooterComponent />





  <!-- <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
  <script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script> -->

</body>

</html>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import { IonIcon } from '@ionic/vue';
import './assets/style/style.css'

import HeaderComponent from './views/HeaderComponent.vue'
import BannerComponent from './views/BannerComponent.vue'
import BannerCategoryComponent from './views/BannerCategoryComponent.vue'
import SideBarCategoryComponents from './views/SideBarCategoryComponents.vue'
import SideBarProductShowCase from './views/SideBarProductShowCase.vue'
import ProductMinimal from './views/ProductMinimal.vue'
import ProductFeatured from './views/ProductFeatured.vue'
import ProductMain from "./views/ProductMain.vue"
import ContainerComponent from './views/ContainerComponent.vue'
import BlogComponent from './views/BlogComponent.vue'
import FooterComponent from './views/FooterComponent.vue'

export default {
  components: {
    HeaderComponent,
    BannerComponent,
    BannerCategoryComponent,
    SideBarCategoryComponents,
    SideBarProductShowCase,
    ProductMinimal,
    ProductFeatured,
    ProductMain,
    ContainerComponent,
    BlogComponent,
    FooterComponent,
  },

  created () {
    console.clear();
    console.log(this.categories);
  },
  
  data() {
    return {
    

      isModalClosed: false,
      isToastClosed: true,
      mobileMenus: Array.from({ length: 3 }, () => ({ isActive: false })),
      isOverlayActive: false,
      // accordionItems: Array.from({ length: 3 }, () => ({ isActive: false })),




    

    };
  },
  methods: {
    test(){
      alert("hi");
    },
    closeModal() {
      this.isModalClosed = true;
    },
    closeToast() {
      this.isToastClosed = true;
    },
    openMobileMenu(index) {
      this.mobileMenus[index].isActive = true;
      this.isOverlayActive = true;
    },
    closeMobileMenu(index) {
      this.mobileMenus[index].isActive = false;
      this.isOverlayActive = false;
    },
    closeMobileMenus() {
      this.mobileMenus.forEach(menu => (menu.isActive = false));
      this.isOverlayActive = false;
    },

  },

};
</script>

    

