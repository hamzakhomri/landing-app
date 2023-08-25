<template>
<div class="container">

<div class="testimonials-box">

  <!--
    - TESTIMONIALS
  -->

  <div class="testimonial">

    <h2 class="title">testimonial</h2>

    <div class="testimonial-card">

      <img src="../assets/images/testimonial-1.jpg" alt="alan doe" class="testimonial-banner" width="80" height="80">

      <p class="testimonial-name">Alan Doe</p>

      <p class="testimonial-title">CEO & Founder Invision</p>

      <img src="../assets/images/icons/quotes.svg" alt="quotation" class="quotation-img" width="26">

      <p class="testimonial-desc">
        Lorem ipsum dolor sit amet consectetur Lorem ipsum
        dolor dolor sit amet.
      </p>

    </div>

  </div>



  <!--
    - CTA
  -->

  <div class="cta-container">

    <img src="../assets/images/cta-banner.jpg" alt="summer collection" class="cta-banner">

    <a href="#" class="cta-content">

      <p class="discount">25% Discount</p>

      <h2 class="cta-title">Summer collection</h2>

      <p class="cta-text">Starting @ $10</p>

      <button class="cta-btn">Shop now</button>

    </a>

  </div>



  <!--
    - SERVICE
  -->

  <div class="service">

    <h2 class="title">Our Services</h2>

    <div class="service-container">

      <a href="#" class="service-item">

        <div class="service-icon">
          <ion-icon name="boat-outline"></ion-icon>
        </div>

        <div class="service-content">

          <h3 class="service-title">Worldwide Delivery</h3>
          <p class="service-desc">For Order Over $100</p>

        </div>

      </a>

      <a href="#" class="service-item">
      
        <div class="service-icon">
          <ion-icon name="rocket-outline"></ion-icon>
        </div>
      
        <div class="service-content">
      
          <h3 class="service-title">Next Day delivery</h3>
          <p class="service-desc">UK Orders Only</p>
      
        </div>
      
      </a>

      <a href="#" class="service-item">
      
        <div class="service-icon">
          <ion-icon name="call-outline"></ion-icon>
        </div>
      
        <div class="service-content">
      
          <h3 class="service-title">Best Online Support</h3>
          <p class="service-desc">Hours: 8AM - 11PM</p>
      
        </div>
      
      </a>

      <a href="#" class="service-item">
      
        <div class="service-icon">
          <ion-icon name="arrow-undo-outline"></ion-icon>
        </div>
      
        <div class="service-content">
      
          <h3 class="service-title">Return Policy</h3>
          <p class="service-desc">Easy & Free Return</p>
      
        </div>
      
      </a>

      <a href="#" class="service-item">
      
        <div class="service-icon">
          <ion-icon name="ticket-outline"></ion-icon>
        </div>
      
        <div class="service-content">
      
          <h3 class="service-title">30% money back</h3>
          <p class="service-desc">For Order Over $100</p>
      
        </div>
      
      </a>

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
  #TESTIMONIAL
  \*-----------------------------------*/
  
  .testimonials-box { margin-bottom: 50px; }
  
  .testimonial-card {
  padding: 30px 20px;
  border: 1px solid var(--cultured);
  border-radius: var(--border-radius-md);
  text-align: center;
  margin-bottom: 25px;
  }
  
  .testimonial-banner {
  margin: auto;
  margin-bottom: 20px;
  border-radius: 50%;
  }
  
  .testimonial-name {
  font-weight: var(--weight-700);
  text-transform: uppercase;
  color: var(--sonic-silver);
  margin-bottom: 5px;
  }
  
  .testimonial-title {
  color: var(--onyx);
  font-size: var(--fs-7);
  margin-bottom: 15px;
  }
  
  .quotation-img {
  margin: auto;
  margin-bottom: 10px;
  }
  
  .testimonial-desc {
  max-width: 70%;
  margin: auto;
  color: var(--sonic-silver);
  font-size: var(--fs-7);
  }
  
  
  @media (min-width: 1024px) {
  
  .testimonials-box {
    display: flex;
    flex-wrap: wrap;
    align-items: stretch;
    gap: 30px;
  }
  
  .testimonial-card { margin-bottom: 0; }
  
  .testimonial {
    min-width: calc(50% - 15px);
    width: calc(50% - 15px);
    margin-bottom: 0;
  }
}


@media (min-width: 1200px) {

  /**
  * #TESTIMONIALS, CTA, SERVICE
  */

  .testimonial{
    min-width: calc(25% - 20px);
    width: calc(25% - 20px);
  }

  .cta-container {
    min-width: calc(50% - 20px);
    width: calc(50% - 20px);
    aspect-ratio: unset;
  }

}



  
</style>