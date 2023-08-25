<template>

<div class="category">

<div class="container">

  <div class="category-item-container has-scrollbar">

    <div class="category-item">

      <div class="category-img-box">
        <img src="../assets/images/icons/dress.svg" alt="dress & frock" width="30">
      </div>

      <div class="category-content-box">

        <div class="category-content-flex">
          <h3 class="category-item-title">Dress & frock</h3>

          <p class="category-item-amount">(53)</p>
        </div>

        <a href="#" class="category-btn">Show all</a>

      </div>

    </div>

    <div class="category-item">

      <div class="category-img-box">
        <img src="../assets/images/icons/coat.svg" alt="winter wear" width="30">
      </div>

      <div class="category-content-box">

        <div class="category-content-flex">
          <h3 class="category-item-title">Winter wear</h3>

          <p class="category-item-amount">(58)</p>
        </div>

        <a href="#" class="category-btn">Show all</a>

      </div>

    </div>

    <div class="category-item">

      <div class="category-img-box">
        <img src="../assets/images/icons/glasses.svg" alt="glasses & lens" width="30">
      </div>

      <div class="category-content-box">

        <div class="category-content-flex">
          <h3 class="category-item-title">Glasses & lens</h3>

          <p class="category-item-amount">(68)</p>
        </div>

        <a href="#" class="category-btn">Show all</a>

      </div>

    </div>

    <div class="category-item">

      <div class="category-img-box">
        <img src="../assets/images/icons/shorts.svg" alt="shorts & jeans" width="30">
      </div>

      <div class="category-content-box">

        <div class="category-content-flex">
          <h3 class="category-item-title">Shorts & jeans</h3>

          <p class="category-item-amount">(84)</p>
        </div>

        <a href="#" class="category-btn">Show all</a>

      </div>

    </div>

    <div class="category-item">

      <div class="category-img-box">
        <img src="../assets/images/icons/tee.svg" alt="t-shirts" width="30">
      </div>

      <div class="category-content-box">

        <div class="category-content-flex">
          <h3 class="category-item-title">T-shirts</h3>

          <p class="category-item-amount">(35)</p>
        </div>

        <a href="#" class="category-btn">Show all</a>

      </div>

    </div>

    <div class="category-item">

      <div class="category-img-box">
        <img src="../assets/images/icons/jacket.svg" alt="jacket" width="30">
      </div>

      <div class="category-content-box">

        <div class="category-content-flex">
          <h3 class="category-item-title">Jacket</h3>

          <p class="category-item-amount">(16)</p>
        </div>

        <a href="#" class="category-btn">Show all</a>

      </div>

    </div>

    <div class="category-item">

      <div class="category-img-box">
        <img src="../assets/images/icons/watch.svg" alt="watch" width="30">
      </div>

      <div class="category-content-box">

        <div class="category-content-flex">
          <h3 class="category-item-title">Watch</h3>

          <p class="category-item-amount">(27)</p>
        </div>

        <a href="#" class="category-btn">Show all</a>

      </div>

    </div>

    <div class="category-item">

      <div class="category-img-box">
        <img src="../assets/images/icons/hat.svg" alt="hat & caps" width="30">
      </div>

      <div class="category-content-box">

        <div class="category-content-flex">
          <h3 class="category-item-title">Hat & caps</h3>

          <p class="category-item-amount">(39)</p>
        </div>

        <a href="#" class="category-btn">Show all</a>

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
  #CATEGORY
  \*-----------------------------------*/
  
  .category { margin-bottom: 30px; }
  
  .category-item-container {
  display: flex;
  align-items: center;
  gap: 10px;
  overflow: auto hidden;
  scroll-snap-type: inline mandatory;
  overscroll-behavior-inline: contain;
  }
  
  .category-item {
  min-width: 100%;
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 15px;
  border: 1px solid var(--cultured);
  border-radius: var(--border-radius-md);
  scroll-snap-align: start;
  }
  
  .category-img-box {
  background: var(--cultured);
  border: 1px solid hsl(0, 0%, 80%);
  padding: 10px;
  border-radius: var(--border-radius-sm);
  }
  
  .category-content-box { width: 100%; }
  
  .category-content-flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 10px;
  }
  
  .category-item-title {
  color: var(--eerie-black);
  font-size: var(--fs-9);
  font-weight: var(--weight-600);
  text-transform: uppercase;
  }
  
  .category-item-amount {
  color: var(--sonic-silver);
  font-size: var(--fs-11);
  }
  
  .category-btn {
  color: var(--salmon-pink);
  font-size: var(--fs-9);
  font-weight: var(--weight-500);
  text-transform: capitalize;
  }


    
  @media (min-width: 570px) {

  

  
/**
 * #CATEGORY
 */

.category-item-container { gap: 30px; }

.category-item { min-width: calc(50% - 15px); }

  }



  @media (min-width: 768px) {
  /*** #CATEGORY */
  .category-img-box { padding: 20px; }
}

@media (min-width: 1024px) {
  /**
   * #CATEGORY 
   */
  
  .category-item { min-width: calc(33.33% - 20px); }
  
  .category-img-box { padding: 10px; }
  
}



@media (min-width: 1200px) {
  
  /**
   * #CATEGORY
   */
  
  .category-item { min-width: calc(25% - 22.5px); }
  
  .category-item-title { --fs-9: 0.824rem; }
  
}
  
</style>