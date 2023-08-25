<template>
     <div class="blog">

<div class="container">

  <div class="blog-container has-scrollbar">

    <div class="blog-card">

      <a href="#">
        <img src="../assets/images/blog-1.jpg" alt="Clothes Retail KPIs 2021 Guide for Clothes Executives" width="300" class="blog-banner">
      </a>

      <div class="blog-content">

        <a href="#" class="blog-category">Fashion</a>

        <a href="#">
          <h3 class="blog-title">Clothes Retail KPIs 2021 Guide for Clothes Executives.</h3>
        </a>

        <p class="blog-meta">
          By <cite>Mr Admin</cite> / <time datetime="2022-04-06">Apr 06, 2022</time>
        </p>

      </div>

    </div>

    <div class="blog-card">
    
      <a href="#">
        <img src="../assets/images/blog-2.jpg" alt="Curbside fashion Trends: How to Win the Pickup Battle."
          class="blog-banner" width="300">
      </a>
    
      <div class="blog-content">
    
        <a href="#" class="blog-category">Clothes</a>
    
        <h3>
          <a href="#" class="blog-title">Curbside fashion Trends: How to Win the Pickup Battle.</a>
        </h3>
    
        <p class="blog-meta">
          By <cite>Mr Robin</cite> / <time datetime="2022-01-18">Jan 18, 2022</time>
        </p>
    
      </div>
    
    </div>

    <div class="blog-card">
    
      <a href="#">
        <img src="../assets/images/blog-3.jpg" alt="EBT vendors: Claim Your Share of SNAP Online Revenue."
          class="blog-banner" width="300">
      </a>
    
      <div class="blog-content">
    
        <a href="#" class="blog-category">Shoes</a>
    
        <h3>
          <a href="#" class="blog-title">EBT vendors: Claim Your Share of SNAP Online Revenue.</a>
        </h3>
    
        <p class="blog-meta">
          By <cite>Mr Selsa</cite> / <time datetime="2022-02-10">Feb 10, 2022</time>
        </p>
    
      </div>
    
    </div>

    <div class="blog-card">
    
      <a href="#">
        <img src="../assets/images/blog-4.jpg" alt="Curbside fashion Trends: How to Win the Pickup Battle."
          class="blog-banner" width="300">
      </a>
    
      <div class="blog-content">
    
        <a href="#" class="blog-category">Electronics</a>
    
        <h3>
          <a href="#" class="blog-title">Curbside fashion Trends: How to Win the Pickup Battle.</a>
        </h3>
    
        <p class="blog-meta">
          By <cite>Mr Pawar</cite> / <time datetime="2022-03-15">Mar 15, 2022</time>
        </p>
    
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
  #BLOG
  \*-----------------------------------*/
  
  .blog { margin-bottom: 30px; }
  
  .blog-container {
  display: flex;
  align-items: flex-start;
  gap: 15px;
  overflow-x: auto;
  overscroll-behavior-inline: contain;
  scroll-snap-type: inline mandatory;
  }
  
  .blog-card {
  min-width: 100%;
  scroll-snap-align: start;
  }
  
  .blog-banner {
  width: 100%;
  border-radius: var(--border-radius-md);
  margin-bottom: 20px;
  }
  
  .blog-category {
  width: max-content;
  color: var(--salmon-pink);
  font-size: var(--fs-8);
  }
  
  .blog-title {
  color: var(--eerie-black);
  font-size: var(--fs-5);
  font-weight: var(--weight-600);
  line-height: 1.4;
  margin-bottom: 5px;
  transition: var(--transition-timing);
  }
  
  .blog-title:hover { color: var(--salmon-pink); }
  
  .blog-meta {
  color: var(--sonic-silver);
  font-size: var(--fs-7);
  }
  
  .blog-meta cite {
  font-style: normal;
  color: var(--davys-gray);
  }
  
  
  @media (min-width: 480px) {
  
  
  /**
   * #BLOG
   */
  
   .blog-container { gap: 30px; }
  
  .blog-card { min-width: calc(50% - 15px); }
  
  @media (min-width: 1024px) {
  
  
  /**
   * #BLOG
   */
  
  .blog-card { min-width: calc(33.33% - 20px); }
  
  .blog-title { --fs-5: 1rem; }
  
}
  }

    
  @media (min-width: 1200px) {
  
  /**
   * #BLOG
   */
  
  .blog { margin-bottom: 50px; }
  
  .blog-card { min-width: calc(25% - 22.5px); }
  
  }
</style>