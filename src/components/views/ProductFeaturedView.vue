<template>
   <div class="product-featured">

<h2 class="title">Deal of the day</h2>

<div class="showcase-wrapper has-scrollbar">

  <div class="showcase-container">

    <div class="showcase">
      
      <div class="showcase-banner">
        <img src="../assets/images/products/shampoo.jpg" alt="shampoo, conditioner & facewash packs" class="showcase-img">
      </div>

      <div class="showcase-content">
        
        <div class="showcase-rating">
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star-outline"></ion-icon>
          <ion-icon name="star-outline"></ion-icon>
        </div>

        <a href="#">
          <h3 class="showcase-title">shampoo, conditioner & facewash packs</h3>
        </a>

        <p class="showcase-desc">
          Lorem ipsum dolor sit amet consectetur Lorem ipsum
          dolor dolor sit amet consectetur Lorem ipsum dolor
        </p>

        <div class="price-box">
          <p class="price">$150.00</p>

          <del>$200.00</del>
        </div>

        <button class="add-cart-btn">add to cart</button>

        <div class="showcase-status">
          <div class="wrapper">
            <p>
              already sold: <b>20</b>
            </p>

            <p>
              available: <b>40</b>
            </p>
          </div>

          <div class="showcase-status-bar"></div>
        </div>

        <div class="countdown-box">

          <p class="countdown-desc">
            Hurry Up! Offer ends in:
          </p>

          <div class="countdown">

            <div class="countdown-content">

              <p class="display-number">360</p>

              <p class="display-text">Days</p>

            </div>

            <div class="countdown-content">
              <p class="display-number">24</p>
              <p class="display-text">Hours</p>
            </div>

            <div class="countdown-content">
              <p class="display-number">59</p>
              <p class="display-text">Min</p>
            </div>

            <div class="countdown-content">
              <p class="display-number">00</p>
              <p class="display-text">Sec</p>
            </div>

          </div>

        </div>

      </div>

    </div>

  </div>

  <div class="showcase-container">
  
    <div class="showcase">
  
      <div class="showcase-banner">
        <img src="../assets/images/products/jewellery-1.jpg" alt="Rose Gold diamonds Earring" class="showcase-img">
      </div>
  
      <div class="showcase-content">
  
        <div class="showcase-rating">
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star-outline"></ion-icon>
          <ion-icon name="star-outline"></ion-icon>
        </div>
  
        <h3 class="showcase-title">
          <a href="#" class="showcase-title">Rose Gold diamonds Earring</a>
        </h3>
  
        <p class="showcase-desc">
          Lorem ipsum dolor sit amet consectetur Lorem ipsum
          dolor dolor sit amet consectetur Lorem ipsum dolor
        </p>
  
        <div class="price-box">
          <p class="price">$1990.00</p>
          <del>$2000.00</del>
        </div>
  
        <button class="add-cart-btn">add to cart</button>
  
        <div class="showcase-status">
          <div class="wrapper">
            <p> already sold: <b>15</b> </p>
  
            <p> available: <b>40</b> </p>
          </div>
  
          <div class="showcase-status-bar"></div>
        </div>
  
        <div class="countdown-box">
  
          <p class="countdown-desc">Hurry Up! Offer ends in:</p>
  
          <div class="countdown">
            <div class="countdown-content">
              <p class="display-number">360</p>
              <p class="display-text">Days</p>
            </div>
  
            <div class="countdown-content">
              <p class="display-number">24</p>
              <p class="display-text">Hours</p>
            </div>
  
            <div class="countdown-content">
              <p class="display-number">59</p>
              <p class="display-text">Min</p>
            </div>
  
            <div class="countdown-content">
              <p class="display-number">00</p>
              <p class="display-text">Sec</p>
            </div>
          </div>
  
        </div>
  
      </div>
  
    </div>
  
  </div>

</div>

</div>
</template>

<script>
export default {

}
</script>

<style>


/*-----------------------------------*\
  #PRODUCT FEATURED
\*-----------------------------------*/

.product-featured { margin-bottom: 30px; }

.product-featured .showcase-wrapper {
  display: flex;
  align-items: center;
  gap: 20px;
  overflow-x: auto;
  overscroll-behavior-inline: contain;
  scroll-snap-type: inline mandatory;
}

.product-featured .showcase-container {
  min-width: 100%;
  padding: 30px;
  border: 1px solid var(--cultured);
  border-radius: var(--border-radius-md);
  scroll-snap-align: start;
}

.product-featured .showcase-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.product-featured .showcase-content { margin-top: 30px; }

.product-featured .showcase-rating {
  color: var(--sandy-brown);
  display: flex;
  align-items: center;
  font-size: 16px;
  margin-bottom: 15px;
}

.product-featured .showcase-title {
  font-size: var(--fs-7);
  color: var(--eerie-black);
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  text-transform: uppercase;
  margin-bottom: 3px;
}

.product-featured .showcase-desc {
  color: var(--sonic-silver);
  font-size: var(--fs-7);
  font-weight: var(--weight-300);
  margin-bottom: 10px;
}

.product-featured .price-box {
  font-size: var(--fs-3);
  display: flex;
  gap: 10px;
  margin-bottom: 10px;
}

.product-featured .price {
  color: var(--salmon-pink);
  font-weight: var(--weight-700);
}

.product-featured del {
  color: var(--sonic-silver);
  font-weight: var(--weight-300);
}

.product-featured .add-cart-btn {
  background: var(--salmon-pink);
  padding: 8px 15px;
  color: var(--white);
  font-weight: var(--fs-9);
  font-weight: var(--weight-700);
  text-transform: uppercase;
  border-radius: var(--border-radius-md);
  margin-bottom: 15px;
  transition: var(--transition-timing);
}

.product-featured .add-cart-btn:hover {
  background: var(--eerie-black);
  color: var(--white);
}

.product-featured .showcase-status { margin-bottom: 15px; }

.product-featured .showcase-status .wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: var(--eerie-black);
  font-size: var(--fs-9);
  font-weight: var(--weight-400);
  text-transform: uppercase;
  margin-bottom: 10px;
}

.product-featured .showcase-status-bar {
  background: var(--cultured);
  position: relative;
  height: 10px;
  border-radius: 5px;
}

.product-featured .showcase-status-bar::before {
  position: absolute;
  content: '';
  top: 3px;
  left: 3px;
  height: 4px;
  width: 40%;
  background: var(--salmon-pink);
  border-radius: 4px;
}

.product-featured .countdown-desc {
  color: var(--eerie-black);
  font-size: var(--fs-9);
  font-weight: var(--weight-600);
  text-transform: uppercase;
  margin-bottom: 10px;
}

.product-featured .countdown {
  display: flex;
  gap: 5px;
}

.product-featured .countdown-content {
  padding: 5px;
  background: var(--cultured);
  border-radius: var(--border-radius-md);
  text-align: center;
}

.product-featured .display-number {
  color: var(--eerie-black);
  font-size: var(--fs-5);
  font-weight: var(--weight-500);
  min-width: 40px;
}

.product-featured .display-text {
  color: var(--davys-gray);
  font-size: var(--fs-11);
}






@media (min-width: 1200px) {
/**
 * #PRODUCT
 */

.product-featured .showcase > div { min-width: calc(50% - 10px); }

.product-featured .display-number { --fs-5: 1.125rem; }

.product-grid { grid-template-columns: repeat(4, 1fr); }

}



@media (min-width: 768px) {
.product-featured .showcase {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
}

.product-featured .showcase-img { max-width: fit-content; }

.product-featured .showcase-content {
  margin-top: 0;
  min-width: calc(100% - 345px);
}}

</style>