<template>
  <div class="modal" :class="{ 'closed': isModalClosed }"  data-modal>

<div class="modal-close-overlay" data-modal-overlay></div>

<div class="modal-content">

  <button @click="closeModal" class="modal-close-btn" data-modal-close>
    <ion-icon name="close-outline"></ion-icon>
  </button>

  <div class="newsletter-img">
    <img src="../assets/images/newsletter.png" alt="subscribe newsletter" width="400" height="400">
  </div>

  <div class="newsletter">

    <form action="#">

      <div class="newsletter-header">

        <h3 class="newsletter-title">Subscribe Newsletter.</h3>
  

        <p class="newsletter-desc">
          Subscribe the <b>Anon</b> to get latest products and discount update.
        </p>

      </div>

      <input type="email" name="email" class="email-field" placeholder="Email Address" required>

      <button type="submit" class="btn-newsletter">Subscribe</button>

    </form>

  </div>

</div>

</div>
</template>

<script>
export default {

    data(){
        return {
            isModalClosed: false,
        }
    },
    methods: {
        closeModal() {
      this.isModalClosed = true;
    },
    },
}
</script>

<style>
  /*** overlay */
  
  .overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: hsla(0, 0%, 0%, 0.5);
  opacity: 0;
  pointer-events: none;
  z-index: 15;
  transition: 0.5s ease;
  }
  
  .overlay.active {
  opacity: 1;
  pointer-events: all;
  }
</style>