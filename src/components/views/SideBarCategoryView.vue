<template>
      <div class="sidebar-category">

<div class="sidebar-top">
  <h2 class="sidebar-title">Category</h2>

  <button class="sidebar-close-btn" data-mobile-menu-close-btn>
    <ion-icon name="close-outline"></ion-icon>
  </button>
</div>
           
<ul class="sidebar-menu-category-list">
  <li class="sidebar-menu-category" v-for="(category, index) in categories" :key="index">
    <button class="sidebar-accordion-menu" @click="toggleAccordionCat(index)">
      <div class="menu-title-flex">
        <img :src="category.icon" :alt="category.name" class="menu-title-img" width="20" height="20">
        <p class="menu-title">{{ category.name }}</p>
      </div>
      <div>
        <ion-icon name="add-outline" v-if="!category.open" class="add-icon"></ion-icon>
        <ion-icon name="remove-outline" v-if="category.open" class="remove-icon"></ion-icon>
      </div>
    </button>
    <ul v-if="category.open" data-accordion>
      <li v-for="product in category.products" :key="product.name">
        <a href="#" class="sidebar-submenu-title">
          <p class="product-name">{{ product.name }}</p>
          <data :value="product.stock" class="stock" title="Available Stock">{{ product.stock }}</data>
        </a>
      </li>
    </ul>

    <ul v-else>
      <p></p>
    </ul>

  </li>
</ul>


      </div> 
      <div class="product-showcase">

<h3 class="showcase-heading">best sellers</h3>

<div class="showcase-wrapper">

  <div class="showcase-container">

    <div class="showcase">

      <a href="#" class="showcase-img-box">
        <img src="../assets/images/products/1.jpg" alt="baby fabric shoes" width="75" height="75"
          class="showcase-img">
      </a>

      <div class="showcase-content">

        <a href="#">
          <h4 class="showcase-title">baby fabric shoes</h4>
        </a>

        <div class="showcase-rating">
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
        </div>

        <div class="price-box">
          <del>$5.00</del>
          <p class="price">$4.00</p>
        </div>

      </div>

    </div>

    <div class="showcase">

      <a href="#" class="showcase-img-box">
        <img src="../assets/images/products/2.jpg" alt="men's hoodies t-shirt" class="showcase-img"
          width="75" height="75">
      </a>

      <div class="showcase-content">

        <a href="#">
          <h4 class="showcase-title">men's hoodies t-shirt</h4>
        </a>
        <div class="showcase-rating">
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star-half-outline"></ion-icon>
        </div>

        <div class="price-box">
          <del>$17.00</del>
          <p class="price">$7.00</p>
        </div>

      </div>

    </div>

    <div class="showcase">

      <a href="#" class="showcase-img-box">
        <img src="../assets/images/products/3.jpg" alt="girls t-shirt" class="showcase-img" width="75"
          height="75">
      </a>

      <div class="showcase-content">

        <a href="#">
          <h4 class="showcase-title">girls t-shirt</h4>
        </a>
        <div class="showcase-rating">
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star-half-outline"></ion-icon>
        </div>

        <div class="price-box">
          <del>$5.00</del>
          <p class="price">$3.00</p>
        </div>

      </div>

    </div>

    <div class="showcase">

      <a href="#" class="showcase-img-box">
        <img src="../assets/images/products/4.jpg" alt="woolen hat for men" class="showcase-img" width="75"
          height="75">
      </a>

      <div class="showcase-content">

        <a href="#">
          <h4 class="showcase-title">woolen hat for men</h4>
        </a>
        <div class="showcase-rating">
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
        </div>

        <div class="price-box">
          <del>$15.00</del>
          <p class="price">$12.00</p>
        </div>

      </div>

    </div>

  </div>

</div>

      </div>
</template>

<script>
export default {
  
    data(){
        return{
            categories: [
        {
          name: 'Footwear',
          icon: 'assets/images/icons/shoes.svg',
          open: false,
          products: [
            { name: 'Sports', stock: 45 },
            { name: 'Formal', stock: 75 },
            { name: 'Casual', stock: 35 },
            { name: 'Safety Shoes', stock: 26 }
          ]
        },
        {
          name: 'Jewelry',
          icon: './assets/images/icons/jewelry.svg',
          open: false,
          products: [
            { name: 'Earrings', stock: 46 },
            { name: 'Couple Rings', stock: 73 },
            { name: 'Necklace', stock: 61 }
          ]
        },
        {
          name: 'Perfume',
          icon: './assets/images/icons/perfume.svg',
          open: false,
          products: [
            { name: 'Clothes Perfume', stock: 12 },
            { name: 'Deodorant', stock: 60 },
            { name: 'jacket', stock: 50 },
            { name: 'dress & frock', stock: 87 }
          ]
        },
        {
          name: 'Cosmetics',
          icon: './assets/images/icons/cosmetics.svg',
          open: false,
          products: [
            { name: 'Shampoo', stock: 68 },
            { name: 'Sunscreen', stock: 46 },
            { name: 'Body Wash', stock: 79 },
            { name: 'Makeup Kit', stock: 23 }
          ]
        },
        {
          name: 'Glasses',
          icon: './assets/images/icons/glasses.svg',
          open: false,
          products: [
            { name: 'Sunglasses', stock: 50 },
            { name: 'Lenses', stock: 48 }
          ]
        },
        {
          name: 'Bags',
          icon: './assets/images/icons/bag.svg',
          open: false,
          products: [
            { name: 'Shopping Bag', stock: 62 },
            { name: 'Gym Backpack', stock: 35 },
            { name: 'Purse', stock: 80 },
            { name: 'Wallet', stock: 75 }
          ]
        }
        // Add more categories and products here
      ],
        }

    },
methods: {
    toggleAccordionCat(index) {
      this.categories[index].open = !this.categories[index].open;
    }
  },
}
</script>

<style>

  
  /*-----------------------------------*\
  #SIDEBAR
  \*-----------------------------------*/
  
  .sidebar {
  background: var(--white);
  position: fixed;
  top: 0;
  left: -100%;
  bottom: 0;
  width: 100%;
  max-width: 320px;
  padding: 30px;
  overflow-y: scroll;
  overscroll-behavior: contain;
  visibility: hidden;
  transition: 0.5s ease;
  z-index: 20;
  }
  
  .sidebar.active {
  left: 0;
  visibility: visible;
  }
  
  .sidebar-category {
  margin-bottom: 15px;
  padding-bottom: 15px;
  border-bottom: 1px solid var(--cultured);
  }
  
  .sidebar-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 10px;
  }
  
  .sidebar-title {
  color: var(--onyx);
  font-size: var(--fs-5);
  text-transform: uppercase;
  letter-spacing: 0.8px;
  font-weight: var(--weight-600);
  }
  
  .sidebar-close-btn {
  color: var(--eerie-black);
  font-size: 22px;
  font-weight: var(--weight-600);
  }
  
  .sidebar-close-btn ion-icon { --ionicon-stroke-width: 50px; }
  
  .sidebar-accordion-menu {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 7px 0;
  }
  
  .sidebar .menu-title-flex {
  display: flex;
  align-items: center;
  gap: 10px;
  }
  
  .sidebar .menu-title {
  font-size: var(--fs-5);
  color: var(--sonic-silver);
  font-weight: var(--weight-500);
  }
  
  .sidebar-accordion-menu ion-icon {
  color: var(--sonic-silver);
  font-size: 14px;
  --ionicon-stroke-width: 70px;
  }
  
  .sidebar-submenu-category-list {
  border-top: 1px solid var(--cultured);
  max-height: 0;
  overflow: hidden;
  visibility: hidden;
  transition: 0.5s ease-in-out;
  }
  
  .sidebar-submenu-category-list.active {
  padding: 13px 0 8px;
  max-height: 122px;
  visibility: visible;
  }
  
  .sidebar-submenu-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: var(--sonic-silver);
  font-size: var(--fs-7);
  padding: 2px 0;
  }
  
  .sidebar-submenu-title:hover { color: var(--eerie-black); }
  
  .sidebar .product-name { text-transform: capitalize; }
  
  .sidebar-accordion-menu.active .add-icon,
  .sidebar-accordion-menu .remove-icon { display: none; }
  
  .sidebar-accordion-menu .add-icon,
  .sidebar-accordion-menu.active .remove-icon { display: block; }
  
  .sidebar .showcase-heading {
  font-size: var(--fs-5);
  font-weight: var(--weight-600);
  color: var(--onyx);
  text-transform: uppercase;
  letter-spacing: 0.8px;
  margin-bottom: 15px;
  }
  
  .sidebar .showcase {
  display: flex;
  align-items: center;
  gap: 15px;
  }
  
  .sidebar .showcase:not(:last-child) { margin-bottom: 15px; }
  
  .sidebar .showcase-img { border-radius: var(--border-radius-sm); }
  
  .sidebar .showcase-content { width: calc(100% - 90px); }
  
  .sidebar .showcase-title {
  color: var(--onyx);
  font-size: var(--fs-7);
  font-weight: var(--weight-400);
  text-transform: capitalize;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  letter-spacing: 0.5px;
  }
  
  .sidebar .showcase-rating {
  display: flex;
  align-items: center;
  color: var(--sandy-brown);
  font-size: 13px;
  padding: 4px 0;
  }
  
  .sidebar .price-box {
  display: flex;
  align-items: center;
  gap: 15px;
  }
  
  .sidebar .price-box del {
  color: var(--sonic-silver);
  font-size: 13px;
  }
  
  .sidebar .price-box .price {
  font-size: var(--fs-7);
  font-weight: var(--weight-600);
  color: var(--davys-gray);
  }
  
  @media (min-width: 1024px) {
  
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
  
  
  }

    
</style>