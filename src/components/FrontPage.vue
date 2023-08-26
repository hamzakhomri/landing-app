<template>


<body>


  <div :class="{ 'active': isOverlayActive }" @click="closeMobileMenus" class="overlay" data-overlay></div>
  <!--- ALERT TO SUBSSCRIBE   -->
  <OverlayView />
  <!--- NOTIFICATION TOAST   -->
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


<style>
  

  :root {
  
  /**
   * colors
   */
  
  --spanish-gray: hsl(0, 0%, 60%);
  --sonic-silver: hsl(0, 0%, 47%);
  --eerie-black: hsl(0, 0%, 13%);
  --salmon-pink: hsl(353, 100%, 78%);
  --sandy-brown: hsl(29, 90%, 65%);
  --bittersweet: hsl(0, 100%, 70%);
  --ocean-green: hsl(152, 51%, 52%);
  --davys-gray: hsl(0, 0%, 33%);
  --cultured: hsl(0, 0%, 93%);
  --white: hsl(0, 100%, 100%);
  --onyx: hsl(0, 0%, 27%);
  
  /**
   * typography
   */
  
  --fs-1: 1.563rem;
  --fs-2: 1.375rem;
  --fs-3: 1.25rem;
  --fs-4: 1.125rem;
  --fs-5: 1rem;
  --fs-6: 0.938rem;
  --fs-7: 0.875rem;
  --fs-8: 0.813rem;
  --fs-9: 0.75rem;
  --fs-10: 0.688rem;
  --fs-11: 0.625rem;
  
  --weight-300: 300;
  --weight-400: 400;
  --weight-500: 500;
  --weight-600: 600;
  --weight-700: 700;
  
  /**
   * border-radius
   */
  
  --border-radius-md: 10px;
  --border-radius-sm: 5px;
  
  /**
   * transition 
   */
  
  --transition-timing: 0.2s ease;
  
  }
  
  
  
  
  
  /*-----------------------------------*\
  #RESET
  \*-----------------------------------*/
  
  *, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }
  
  a { text-decoration: none; }
  
  li { list-style: none; }
  
  button {
  background: none;
  font: inherit;
  border: none;
  cursor: pointer;
  }
  
  img, ion-icon, button, a { display: block; }
  
  span { display: inline-block; }
  
  html {
  font-family: "Poppins", sans-serif;
  overscroll-behavior: contain;
  }
  
  input {
  display: block;
  width: 100%;
  font: inherit;
  }
  
  input::placeholder { font: inherit; }
  
  body { background: var(--white); }
  
  /**
  * scrollbar style
  */
  
  body::-webkit-scrollbar { width: 15px; }
  
  body::-webkit-scrollbar-track {
  background: var(--white);
  border-left: 1px solid var(--cultured);
  }
  
  body::-webkit-scrollbar-thumb {
  background: hsl(0, 0%, 80%);
  border: 3px solid var(--white);
  border-radius: 10px;
  }
  
  body::-webkit-scrollbar-thumb:hover { background: hsl(0, 0%, 70%); }
  
  
  
  
  /*-----------------------------------*\
  #REUSED STYLE
  \*-----------------------------------*/
  
  .container { padding: 0 15px; }
  
  .has-scrollbar { padding-bottom: 5px; }
  
  .has-scrollbar::-webkit-scrollbar {
  width: 12px; /* for vertical scroll */
  height: 12px; /* for horizontal scroll */
  }
  
  .has-scrollbar::-webkit-scrollbar-thumb {
  background: transparent;
  border: 3px solid var(--white);
  border-radius: 20px;
  }
  
  .has-scrollbar:hover::-webkit-scrollbar-thumb { background: hsl(0, 0%, 90%); }
  
  .has-scrollbar::-webkit-scrollbar-thumb:hover { background: hsl(0, 0%, 80%); }
  
  .title {
  color: var(--eerie-black);
  font-size: var(--fs-5);
  font-weight: var(--weight-600);
  letter-spacing: 0.4px;
  text-transform: capitalize;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--cultured);
  margin-bottom: 30px;
  }
  
  
  
  
  
  /*-----------------------------------*\
  #MAIN
  \*-----------------------------------*/
  

  
  
  
  /**
  * MODAL 
  */
  
  .modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: hsla(0, 0%, 0%, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  visibility: hidden;
  pointer-events: none;
  z-index: 10;
  animation: popup 1s ease-in-out 5s forwards;
  }
  
  @keyframes popup {
  
  0% {
    opacity: 0;
    visibility: hidden;
    pointer-events: none;
  }
  
  100% {
    opacity: 1;
    visibility: visible;
    pointer-events: all;
  }
  
  }
  
  .modal.closed { display: none; }
  
  .modal-close-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  }
  
  .newsletter-img { display: none; }
  
  .modal-content {
  position: relative;
  max-width: 350px;
  margin: 20px;
  background: var(--white);
  border-radius: var(--border-radius-md);
  overflow: hidden;
  z-index: 2;
  animation: scaleUp 0.5s ease-in-out 5s forwards;
  }
  
  @keyframes scaleUp {
  
  0% { transform: scale(0.9); }
  100% { transform: scale(1); }
  
  }
  
  .modal-close-btn {
  position: absolute;
  top: 15px;
  right: 15px;
  background: var(--salmon-pink);
  color: var(--white);
  font-size: 16px;
  padding: 5px;
  border-radius: var(--border-radius-sm);
  }
  
  .modal-close-btn:hover { opacity: 0.9; }
  
  .modal-close-btn ion-icon { --ionicon-stroke-width: 70px; }
  
  .newsletter {
  padding: 50px 30px;
  text-align: center;
  }
  
  .newsletter-header { margin-bottom: 20px; }
  
  .newsletter-title {
  color: var(--onyx);
  font-size: var(--fs-2);
  font-weight: var(--weight-600);
  margin-bottom: 10px;
  }
  
  .newsletter-desc {
  color: var(--sonic-silver);
  font-size: var(--fs-7);
  line-height: 1.6;
  }
  
  .email-field {
  font-size: var(--fs-7);
  padding: 8px 16px;
  border-radius: var(--border-radius-sm);
  border: 1px solid var(--cultured);
  margin-bottom: 16px;
  }
  
  .btn-newsletter {
  background: var(--eerie-black);
  color: var(--white);
  font-size: var(--fs-7);
  font-weight: var(--weight-600);
  text-transform: uppercase;
  padding: 10px 15px;
  border-radius: var(--border-radius-sm);
  margin: auto;
  transition: var(--transition-timing);
  }
  
  .btn-newsletter:hover { background: var(--salmon-pink); }
  
  
  
  
  
  /**
  * NOTIFICATION TOAST 
  */
  
  .notification-toast {
  position: fixed;
  bottom: 80px;
  left: 20px;
  right: 20px;
  background: var(--white);
  max-width: 300px;
  display: flex;
  align-items: flex-start;
  gap: 15px;
  padding: 15px;
  border-radius: var(--border-radius-md);
  box-shadow: 0 5px 20px hsla(0, 0%, 0%, 0.15);
  transform: translateX(calc(-100% - 40px));
  transition: 0.5s ease-in-out;
  z-index: 5;
  animation: slideInOut 10s ease-in-out infinite;
  }
  
  @keyframes slideInOut {
  
  0%,
  45%,
  100% {
    transform: translateX(calc(-100% - 40px));
    opacity: 0;
    visibility: hidden;
  }
  
  50%,
  95% {
    transform: translateX(0);
    opacity: 1;
    visibility: visible;
  }
  
  }
  
  .notification-toast.closed { display: none; }
  
  .toast-close-btn {
  position: absolute;
  top: 10px;
  right: 10px;
  color: var(--sonic-silver);
  }
  
  .toast-close-btn ion-icon { --ionicon-stroke-width: 50px; }
  
  .toast-banner {
  width: 70px;
  height: 70px;
  border: 1px solid var(--cultured);
  border-radius: var(--border-radius-sm);
  }
  
  .toast-banner img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  object-position: center;
  }
  
  .toast-detail {
  width: calc(100% - 85px);
  padding-right: 10px;
  }
  
  .toast-message {
  font-size: var(--fs-10);
  color: var(--sonic-silver);
  margin-bottom: 8px;
  }
  
  .toast-title {
  font-size: var(--fs-7);
  font-weight: var(--weight-500);
  color: var(--onyx);
  }
  
  .toast-meta {
  font-size: var(--fs-10);
  color: var(--sonic-silver);
  }
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  /*-----------------------------------*\
  #CTA
  \*-----------------------------------*/
  
  .cta-container {
  position: relative;
  aspect-ratio: 5 / 6;
  border-radius: var(--border-radius-md);
  overflow: hidden;
  margin-bottom: 25px;
  }
  
  .cta-banner {
  width: 100%;
  height: 100%;
  object-fit: cover;
  }
  
  .cta-content {
  background: hsla(0, 0%, 100%, 0.7);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: fit-content;
  padding: 15px 20px;
  text-align: center;
  border-radius: var(--border-radius-sm);
  }
  
  .cta-content .discount {
  background: var(--eerie-black);
  color: var(--white);
  font-size: var(--fs-11);
  font-weight: var(--weight-600);
  text-transform: uppercase;
  width: max-content;
  margin: auto;
  padding: 0 5px;
  border-radius: var(--border-radius-sm);
  margin-bottom: 5px;
  }
  
  .cta-title {
  color: var(--onyx);
  font-size: var(--fs-5);
  text-transform: capitalize;
  margin-bottom: 5px;
  }
  
  .cta-text {
  color: var(--sonic-silver);
  font-size: var(--fs-7);
  margin-bottom: 5px;
  }
  
  .cta-btn {
  font-size: var(--fs-9);
  color: var(--sonic-silver);
  text-transform: uppercase;
  font-weight: var(--weight-700);
  margin: auto;
  }
  
  
  
  
  
  /*-----------------------------------*\
  #SERVICE
  \*-----------------------------------*/
  
  .service-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 30px;
  padding: 30px 15px;
  border: 1px solid var(--cultured);
  border-radius: var(--border-radius-md);
  }
  
  .service-item {
  min-width: 190px;
  display: flex;
  align-items: center;
  gap: 15px;
  }
  
  .service-icon {
  font-size: 35px;
  color: var(--salmon-pink);
  transition: var(--transition-timing);
  }
  
  .service-icon ion-icon { --ionicon-stroke-width: 25px; }
  
  .service-item:hover .service-icon { color: var(--eerie-black); }
  
  .service-title {
  color: var(--sonic-silver);
  font-size: var(--fs-7);
  font-weight: var(--weight-600);
  text-transform: capitalize;
  margin-bottom: 5px;
  }
  
  .service-desc {
  color: var(--sonic-silver);
  font-size: var(--fs-9);
  }
  
  
  
  
  
  
  
  /*-----------------------------------*\
  #RESPONSIVE
  \*-----------------------------------*/
  /*** responsive larger than 480px screen*/
  
  @media (min-width: 480px) {
  /*** #CUSTOM PROPERTY*/
  
  :root {
  
    /*** typography */
  
    --fs-1: 1.875rem;
  }
  /*** #CTA*/
  
  .cta-content { padding: 40px; }
  
  .cta-content .discount {
    --fs-11: 0.875rem;
    padding: 5px 10px;
  }
  
  .cta-title { --fs-5: 1.5rem; }
  
  .cta-text { --fs-7: 1rem; }
  
  .cta-btn { --fs-9: 1rem; }
  
  
  }
  

  /*** responsive larger than 570px screen*/
  
  @media (min-width: 570px) {
  /*** #CTA*/
  
  .cta-container { aspect-ratio: 6 / 5; }
  }


  /*** responsive larger than 768px screen*/
  @media (min-width: 768px) {
  
  /*** #CUSTOM PROPERTY*/
  
  :root {
    /*** typography */
    --fs-1: 2.375rem;
  }
  /*** #BASE */
  
  html { font-size: 17px; }
  
  /*** #REUSED STYLE */
  
  .container {
    max-width: 750px;
    margin: auto;
  }
  
  /*** #MODAL */
  
  .modal-content {
    display: flex;
    align-items: center;
    max-width: 750px;
    width: fit-content;
  }
  
  .newsletter-img { display: block; }
  
  .newsletter { text-align: left; }
  
  }
  

  /*** responsive larger than 1024px screen*/
  @media (min-width: 1024px) {
  
  /*** #CUSTOM PROPERTY*/
  
  :root {
    /*** typography */
  
    --fs-1: 2.625rem;
    --fs-2: 1.125rem;
  
  }
  

  /*** #REUSED STYLE */
  
  .container { max-width: 980px; }
  /*** #NOTIFICATION TOAST */
  
  .notification-toast { bottom: 30px; }
  
  
  
  /*** #PRODUCT */
  
  .product-container .container {
    position: relative;
    display: flex;
    align-items: flex-start;
    gap: 30px;
    margin-bottom: 30px;
  }
  
  .sidebar {
    --fs-5: 0.941rem;
  
    position: sticky;
    top: 30px;
    left: 0;
    padding: 0;
    min-width: calc(25% - 15px);
    margin-bottom: 30px;
    visibility: visible;
    overflow-y: auto;
    overscroll-behavior: auto;
    z-index: 0;
  }
  
  .sidebar-category {
    padding: 20px;
    margin-bottom: 30px;
    border: 1px solid var(--cultured);
    border-radius: var(--border-radius-md);
  }
  
  .sidebar-close-btn { display: none; }
  
  .product-box { min-width: calc(75% - 15px); }
  
  .product-minimal { margin-bottom: 20px; }
  
  .product-minimal .product-showcase {
    min-width: calc(33.33% - 14px);
    width: calc(33.33% - 14px);
    flex-grow: 1;
  }
  
  .product-minimal .showcase-wrapper { gap: 10px; }
  
  .product-minimal .showcase-container { padding: 2px; }
  
  
  .product-grid { grid-template-columns: repeat(3, 1fr); }
  
  
  .cta-container {
    min-width: calc(50% - 15px);
    width: calc(50% - 15px);
    margin-bottom: 0;
  }
  
  .service { width: 100%; }
  
  .service-container { gap: 0; }
  
  .service-item {
    flex-direction: column;
    text-align: center;
    min-width: 20%;
  }
  

  
  }


  /*** responsive larger than 1200px screen*/
  @media (min-width: 1200px) {
  
      /*** #REUSED STYLE */
      
      .container { max-width: 1200px; }
      
      /*** #CTA, SERVICE*/
      .service {
        min-width: calc(25% - 20px);
        width: calc(25% - 20px);
      }
      
      .cta-container {
        min-width: calc(50% - 20px);
        width: calc(50% - 20px);
        aspect-ratio: unset;
      }
      
      .service-container {
        justify-content: flex-start;
        gap: 16px;
        padding: 30px;
      }
      
      .service-item {
        flex-direction: row;
        text-align: left;
      }
  }
  

  /*** responsive larger than 1400px screen*/
  @media (min-width: 1400px) {
  
  /**
   * #BASE 
   */
  
  html { font-size: 18px; }
  
  /**
   * #REUSED STYLE 
   */
  
  .container { max-width: 1350px; }
  
  }
    
</style>

    

