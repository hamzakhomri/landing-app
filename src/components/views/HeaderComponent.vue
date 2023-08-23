<template>

    
    <div class="header-top">

      <div class="container">

        <ul class="header-social-container">

          <li>
            <a href="#" class="social-link">
              <ion-icon name="logo-facebook"></ion-icon>
            </a>
          </li>

          <li>
            <a href="#" class="social-link">
              <ion-icon name="logo-twitter"></ion-icon>
            </a>
          </li>

          <li>
            <a href="#" class="social-link">
              <ion-icon name="logo-instagram"></ion-icon>
            </a>
          </li>

          <li>
            <a href="#" class="social-link">
              <ion-icon name="logo-linkedin"></ion-icon>
            </a>
          </li>

        </ul>

        <div class="header-alert-news">
          <p>
            <b>Free Shipping</b>
            This Week Order Over - $55
          </p>
         
          
        </div>

        <!-- <div class="header-top-actions">

          <select name="currency">

            <option value="usd">USD &dollar;</option>
            <option value="eur">EUR &euro;</option>

          </select>

          <select name="language">

            <option value="en-US">English</option>
            <option value="es-ES">Espa&ntilde;ol</option>
            <option value="fr">Fran&ccedil;ais</option>

          </select>

        </div> -->

      </div>

    </div>

    <div class="header-main">

      <div class="container">

        <a href="#" class="header-logo">
          <img src="../assets/images/logo/logo_complet_black.svg" alt="Anon's logo" width="120" height="36">
        </a>

        <div class="header-search-container">

          <input type="search" name="search" class="search-field" placeholder="Enter your product name...">

          <button class="search-btn">
            <ion-icon name="search-outline"></ion-icon>
          </button>

        </div>

        <div class="header-user-actions">

          <button class="action-btn">
            <ion-icon name="person-outline"></ion-icon>
          </button>

          <button class="action-btn">
            <ion-icon name="heart-outline"></ion-icon>
            <span class="count">0</span>
          </button>

          <button class="action-btn">
            <ion-icon name="bag-handle-outline"></ion-icon>
            <span class="count">0</span>
          </button>

        </div>

      </div>

    </div>

    <nav class="desktop-navigation-menu">

      <div class="container">

        <ul class="desktop-menu-category-list">

          <li class="menu-category">
            <a href="#" class="menu-title">Home</a>
          </li>

          <li class="menu-category">
            <a href="#" class="menu-title">Categories</a>

            <div class="dropdown-panel">

              <ul class="dropdown-panel-list">
                  <li class="menu-title">
                    <a href="#">Les piéces</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Carénages</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#"></a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Piéces moteur</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Pneus</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Trouver une piece</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">autres</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">
                      <img src="../assets/images/accessoires-banner2.jpg" alt="headphone collection" width="250"
                        height="119">
                    </a>
                  </li>
              </ul>



              <ul class="dropdown-panel-list">
                  <li class="menu-title">
                    <a href="#">Accessoires</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Miroirs</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Poignets</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Phares secours</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">cache poignée </a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Autres</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">
                      <img src="../assets/images/accessoires-banner5.webp" alt="men's fashion" width="250" height="119">
                    </a>
                  </li>
              </ul>
       

              <ul class="dropdown-panel-list">
                  <li class="menu-title">
                    <a href="#">Women's</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Formal</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Casual</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Perfume</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Cosmetics</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Bags</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">
                      <img src="../assets/images/womens-banner.jpg" alt="women's fashion" width="250" height="119">
                    </a>
                  </li>
              </ul>


              <ul class="dropdown-panel-list">
                  <li class="menu-title">
                    <a href="#">Electronics</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Smart Watch</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Smart TV</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Keyboard</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Mouse</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">Microphone</a>
                  </li>

                  <li class="panel-list-item">
                    <a href="#">
                      <img src="../assets/images/electronics-banner-2.jpg" alt="mouse collection" width="250" height="119">
                    </a>
                  </li>
              </ul>

            </div>
          </li>



          <li class="menu-category">
            <a href="#" class="menu-title">Men's</a>

            <ul class="dropdown-list">
              <li class="dropdown-item">
                <a href="#">Shirt</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Shorts & Jeans</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Safety Shoes</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Wallet</a>
              </li>
            </ul>
          </li>



          <li class="menu-category">
            <a href="#" class="menu-title">Women's</a>
            <ul class="dropdown-list">

              <li class="dropdown-item">
                <a href="#">Dress & Frock</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Earrings</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Necklace</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Makeup Kit</a>
              </li>
            </ul>
          </li>



          <li class="menu-category">
            <a href="#" class="menu-title">Jewelry</a>
            <ul class="dropdown-list">

              <li class="dropdown-item">
                <a href="#">Earrings</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Couple Rings</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Necklace</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Bracelets</a>
              </li>

            </ul>
          </li>



          <li class="menu-category">
            <a href="#" class="menu-title">Perfume</a>        
            <ul class="dropdown-list">

              <li class="dropdown-item">
                <a href="#">Clothes Perfume</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Deodorant</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Flower Fragrance</a>
              </li>

              <li class="dropdown-item">
                <a href="#">Air Freshener</a>
              </li>
            </ul>
          </li>


          <li class="menu-category">
            <a href="#" class="menu-title">Blog</a>
          </li>

          <li class="menu-category">
            <a href="#" class="menu-title">Hot Offers</a>
          </li>

        </ul>
      </div>
    </nav>
    <template v-for="(menu, index) in mobileMenus" :key="index">

      <div  class="mobile-bottom-navigation">

        <button @click="openMobileMenu(index)" data-mobile-menu-open-btn>
          <ion-icon name="menu-outline"></ion-icon>
        </button>

        <button class="action-btn" >
          <ion-icon name="bag-handle-outline"></ion-icon>
          <span class="count">0</span>
        </button>

        <button class="action-btn">
          <ion-icon name="home-outline"></ion-icon>
        </button>

        <button class="action-btn">
          <ion-icon name="heart-outline"></ion-icon>

          <span class="count">0</span>
        </button>

        <button class="action-btn" data-mobile-menu-open-btn>
          <ion-icon name="grid-outline"></ion-icon>
        </button>

      </div>

      <nav class="mobile-navigation-menu has-scrollbar" :class="{ 'active': menu.isActive }" data-mobile-menu>

        <div class="menu-top">
          <h2 class="menu-title">Menu</h2>

          <button class="menu-close-btn"  @click="closeMobileMenu(index)" data-mobile-menu-close-btn>
            <ion-icon name="close-outline"></ion-icon>
          </button>
        </div>

        <template v-for="(item, index) in accordionItems" :key="index">
          <li class="menu-category">
            <button @click="toggleAccordion(index)" data-accordion-btn class="accordion-button">
              <div class="accordion-menu-navig" data-accordion-btn> 
                <p class="menu-title">{{ item.title }}</p>
                <ion-icon v-if="!item.isActive" name="add-outline" class="icon"></ion-icon>
                <ion-icon v-if="item.isActive" name="remove-outline" class="icon"></ion-icon>
              </div>
            </button>
            <ul class="submenu-category-list" :class="{ 'active': item.isActive }" data-accordion>
              <li class="submenu-category" v-for="(submenu, subIndex) in item.submenus" :key="subIndex">
                <a href="#" class="submenu-title">{{ submenu.title }}</a>
              </li>
            </ul>
          </li>
        </template>


        <div class="menu-bottom">

          <ul class="menu-category-list">

            <li class="menu-category">

              <button class="accordion-menu" data-accordion-btn>
                <p class="menu-title">Language</p>

                <ion-icon name="caret-back-outline" class="caret-back"></ion-icon>
              </button>

              <ul class="submenu-category-list" data-accordion>

                <li class="submenu-category">
                  <a href="#" class="submenu-title">English</a>
                </li>

                <li class="submenu-category">
                  <a href="#" class="submenu-title">Espa&ntilde;ol</a>
                </li>

                <li class="submenu-category">
                  <a href="#" class="submenu-title">Fren&ccedil;h</a>
                </li>

              </ul>

            </li>

            <li class="menu-category">
              <button class="accordion-menu" data-accordion-btn>
                <p class="menu-title">Currency</p>
                <ion-icon name="caret-back-outline" class="caret-back"></ion-icon>
              </button>

              <ul class="submenu-category-list" data-accordion>
                <li class="submenu-category">
                  <a href="#" class="submenu-title">USD &dollar;</a>
                </li>

                <li class="submenu-category">
                  <a href="#" class="submenu-title">EUR &euro;</a>
                </li>
              </ul>
            </li>

          </ul>

          <ul class="menu-social-container">

            <li>
              <a href="#" class="social-link">
                <ion-icon name="logo-facebook"></ion-icon>
              </a>
            </li>

            <li>
              <a href="#" class="social-link">
                <ion-icon name="logo-twitter"></ion-icon>
              </a>
            </li>

            <li>
              <a href="#" class="social-link">
                <ion-icon name="logo-instagram"></ion-icon>
              </a>
            </li>

            <li>
              <a href="#" class="social-link">
                <ion-icon name="logo-linkedin"></ion-icon>
              </a>
            </li>

          </ul>

        </div>

      </nav>
    </template>
    </template>

<script>
import '../assets/style/style.css'
export default {
    data(){
        return{
            mobileMenus: Array.from({ length: 3 }, () => ({ isActive: false })),

            accordionItems: [
                    {
                    title: "Men's",
                    isActive: false,
                    submenus: [
                        { title: 'Shirt' },
                        { title: 'Shorts & Jeans' },
                        { title: 'Safety Shoes' },
                        { title: 'Wallet' }
                    ]
                    },
                    {
                    title: "Women's",
                    isActive: false,
                    submenus: [
                        { title: 'Dress & Frock' },
                        { title: 'Earrings' },
                        { title: 'Necklace' },
                        { title: 'Makeup Kit' }
                    ]
                    },
                ],
        }
    },
    
  methods: {
    closeMobileMenu(index) {
      this.mobileMenus[index].isActive = false;
      this.isOverlayActive = false;
    },
    openMobileMenu(index) {
      this.mobileMenus[index].isActive = true;
      this.isOverlayActive = true;
    },
  },
    
}
</script>

<style>

</style>