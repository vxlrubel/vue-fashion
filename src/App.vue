<script setup>
  import { RouterLink, RouterView } from 'vue-router';
  import IconBar from './components/icons/IconBar.vue';
  import MinicartIcon from './components/MinicartIcon.vue';
  import UserDropdown from './components/UserDropdown.vue';
</script>

<template>
  <header class="clearfix bg-light border-bottom shadow-sm">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-6 col-md-12 col-lg-3">
          <div class="text-md-center text-lg-start">
            <RouterLink to="/" class="text-secondary text-decoration-none fs-4">VueFashion</RouterLink>
          </div>
        </div>
        <div class="col-md-8 col-lg-6 d-none d-md-block">
          <ul class="list-unstyled d-flex m-0 p-0">
            <li class="me-1"><RouterLink to="/" class="text-secondary text-decoration-none px-3 py-3 d-flex align-items-center">Home</RouterLink></li>
            <li class="me-1"><RouterLink to="/products" class="text-secondary text-decoration-none px-3 py-3 d-flex align-items-center">Products</RouterLink></li>
          </ul>
        </div>
        <div class="col-6 col-md-4 col-lg-3 py-1 py-md-0">
          <div class="d-flex justify-content-end">
            <div class="dropdown d-inline-flex d-md-none">
              <button type="button" class="btn border-0 shadow-none" data-bs-toggle="collapse" data-bs-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
                <span class="icon"><IconBar /></span>
              </button>
            </div>


            <MinicartIcon/>
            <UserDropdown/>

          </div>
          
        </div>
      </div>
    </div>

    <!-- collapse menu -->
    <div class="collapse" id="collapseExample">
      <div class="card card-body">
        Some placeholder content for the collapse component. This panel is hidden by default but revealed when the user activates the relevant trigger.
      </div>
    </div>

    
    <!-- minicart -->
    <div class="offcanvas offcanvas-end" tabindex="-1" id="minicart" aria-labelledby="shoppingCartTitle">
      <div class="offcanvas-header px-4">
        <div class="d-flex" id="shoppingCartTitle">
          <h4 class="fs-5 m-0">Shopping Cart</h4>
          <div class="ms-2">items-12</div>
        </div>
        <button type="button" class="btn-close shadow-none" data-bs-dismiss="offcanvas" aria-label="Close"></button>
      </div>
      <div class="offcanvas-body px-4">
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
      </div>
      <div class="offcanvas-footer px-4 py-3">
        <div class="row">
          <div class="col-6">
            <a href="javascript:void(0)" class="btn btn-sm w-100 btn-primary rounded-0">View Cart</a>
          </div>
          <div class="col-6">
            <a href="javascript:void(0)" class="btn btn-sm w-100 btn-outline-primary rounded-0">Checkout</a>
          </div>
        </div>
      </div>
    </div>
      
  </header>

  <RouterView />
 
</template>

<style scoped>
</style>
