<template>
  <div class="banner">

<div class="container">

  <div class="slider-container has-scrollbar">

    <div class="slider-item">

      <img src="../assets/images/home_image_1.jpg" alt="women's latest fashion sale" class="banner-img">

      <div class="banner-content">

        <p class="banner-subtitle">Trending item</p>
        
        <h2 class="banner-title">Women's latest fashion sale</h2>

        <p class="banner-text">
          starting at &dollar; <b>20</b>.00
        </p>

        <a href="#" class="banner-btn">Shop now</a>

      </div>

    </div>

    <div class="slider-item">

      <img src="../assets/images/home_image_2.jpg" alt="modern sunglasses" class="banner-img">

      <div class="banner-content">

        <p class="banner-subtitle">Trending accessories</p>

        <h2 class="banner-title">Modern sunglasses</h2>

        <p class="banner-text">
          starting at &dollar; <b>15</b>.00
        </p>

        <a href="#" class="banner-btn">Shop now</a>

      </div>

    </div>

    <div class="slider-item">

      <img src="../assets/images/home_image_3.jpg" alt="new fashion summer sale" class="banner-img">

      <div class="banner-content">

        <p class="banner-subtitle">Sale Offer</p>

        <h2 class="banner-title">New fashion summer sale</h2>

        <p class="banner-text">
          starting at &dollar; <b>29</b>.99
        </p>

        <a href="#" class="banner-btn">Shop now</a>

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
  #BANNER
  \*-----------------------------------*/
  
  .banner { margin: 30px 0; }
  
  .slider-container {
  display: flex;
  align-items: center;
  gap: 10px;
  border-radius: var(--border-radius-md);
  overflow: auto hidden;
  scroll-snap-type: inline mandatory;
  overscroll-behavior-inline: contain;
  }
  
  .slider-item {
  position: relative;
  min-width: 100%;
  max-height: 450px;
  aspect-ratio: 1 / 1;
  border-radius: var(--border-radius-md);
  overflow: hidden;
  scroll-snap-align: start;
  }
  
  .slider-item .banner-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: right;
  }
  
  .banner-content {
  background: hsla(0, 0%, 100%, 0.8);
  position: absolute;
  bottom: 25px;
  left: 25px;
  right: 25px;
  padding: 20px 25px;
  border-radius: var(--border-radius-md);
  }
  
  .banner-subtitle {
  color: var(--salmon-pink);
  font-size: var(--fs-7);
  font-weight: var(--weight-500);
  text-transform: capitalize;
  letter-spacing: 2px;
  margin-bottom: 10px;
  }
  
  .banner-title {
  color: var(--eerie-black);
  font-size: var(--fs-1);
  text-transform: uppercase;
  line-height: 1;
  margin-bottom: 10px;
  }
  
  .banner-text { display: none; }
  
  .banner-btn {
  background: var(--salmon-pink);
  color: var(--white);
  width: max-content;
  font-size: var(--fs-11);
  font-weight: var(--weight-600);
  text-transform: uppercase;
  padding: 4px 10px;
  border-radius: var(--border-radius-sm);
  transition: var(--transition-timing);
  }
  
  .banner-btn:hover { background: var(--eerie-black); }

  @media (min-width: 570px) {

  
/**
 * #BANNER
 */

.slider-item { aspect-ratio: 4 / 2; }

.banner-content { background: none; }

  }


  @media (min-width: 480px) {
  

  
  
  
  /**
   * #BANNER
   */
  
  .slider-item { aspect-ratio: 5 / 3; }
  
  .banner-content {
    top: 50%;
    right: auto;
    bottom: auto;
    transform: translateY(-50%);
    max-width: 320px;
  }
  
  .banner-subtitle { --fs-7: 1rem; }
  
  .banner-text {
    display: block;
    color: var(--sonic-silver);
    font-size: var(--fs-7);
    font-weight: var(--weight-500);
    margin-bottom: 10px;
  }
  
  .banner-text b { font-size: var(--fs-2); }
  
  .banner-btn { padding: 7px 20px; }
}









@media (min-width: 768px) {
  
  /**
   * #BANNER 
   */
  
  .slider-item {
    aspect-ratio: auto;
    height: 350px;
  }
  
  .banner-content { max-width: 380px; }
  
  .banner-subtitle { --fs-7: 1.25rem; }
  
  .banner-text { --fs-7: 1.125rem; }
  
  .banner-text b { --fs-2: 1.875rem; }
  
  .banner-btn { --fs-11: 0.75rem; }
  
}
  
@media (min-width: 1024px) {
  
  
  /**
   * #BANNER 
   */
  
  .banner { margin-top: 0; }
  
  .slider-item { height: 380px; }
  
  .banner-content {
    left: 75px;
    max-width: 400px;
  }
  
  .banner-subtitle { --fs-7: 1.625rem; }
  
  .banner-text { --fs-7: 1.375rem; }
  
  .banner-btn { --fs-11: 0.875rem; }
}

  
@media (min-width: 1200px) {
  
  /**
   * #BANNER
   */
  
  .slider-item:last-child 
  .banner-img { object-position: top; }
  
}
</style>