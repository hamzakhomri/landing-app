<template>


<body>


  <div :class="{ 'active': isOverlayActive }" @click="closeMobileMenus" class="overlay" data-overlay></div>

  <!--- ALERT TO SUBSSCRIBE   -->

  <OverlayView />

  <!---    NOTIFICATION TOAST   -->

 <NotificationToast />

      <HeaderView /> 
    
  <main>
    <BannerView />
    <BannerCategoryView />

    <div class="product-container">

      <div class="container">
        <!-- - SIDEBAR -->
        <div class="sidebar  has-scrollbar" data-mobile-menu>

          <SideBarCategoryView />
          <SideBarProductShowCaseView />
        </div>

        <div class="product-box">

          <ProductMinimalView />
          <ProductFeaturedView />
          <ProductMainView />

        </div>

      </div>

    </div>

    <div>
      <ContainerView />
    </div>

    <BlogView />
   

  </main>

 <FooterView />

</body>


</template>

<script>
import './assets/style/style.css'

import HeaderView from './views/HeaderView.vue'
import BannerView from './views/BannerView.vue'
import BannerCategoryView from './views/BannerCategoryView.vue'
import SideBarCategoryView from './views/SideBarCategoryView.vue'
import SideBarProductShowCaseView from './views/SideBarProductShowCaseView.vue'
import ProductMinimalView from './views/ProductMinimalView.vue'
import ProductFeaturedView from './views/ProductFeaturedView.vue'
import ProductMainView from "./views/ProductMainView.vue"
import ContainerView from './views/ContainerView.vue'
import BlogView from './views/BlogView.vue'
import FooterView from './views/FooterView.vue'
import OverlayView from './views/OverlayView.vue'
import NotificationToast from './views/NotificationToastView.vue'

export default {
  components: {
    HeaderView,
    BannerView,
    BannerCategoryView,
    SideBarCategoryView,
    SideBarProductShowCaseView,
    ProductMinimalView,
    ProductFeaturedView,
    ProductMainView,
    ContainerView,
    BlogView,
    FooterView,
    OverlayView,
    NotificationToast,
  },

  created () {
  },
  
  data() {
    return {
      mobileMenus: Array.from({ length: 3 }, () => ({ isActive: false })),
      isOverlayActive: false,
      // accordionItems: Array.from({ length: 3 }, () => ({ isActive: false })),

    };
  },
  methods: {
    // openMobileMenu(index) {
    //   this.mobileMenus[index].isActive = true;
    //   this.isOverlayActive = true;
    // },
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

    

