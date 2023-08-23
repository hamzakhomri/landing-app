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

</style>