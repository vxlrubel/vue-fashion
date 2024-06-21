<script setup>
  import { RouterLink, RouterView } from 'vue-router';
  import Iconuser from './components/icons/IconUser.vue';
  import IconCart from './components/icons/IconCart.vue';
  import IconBar from './components/icons/IconBar.vue';
</script>

<template>
  <header class="clearfix bg-light border-bottom shadow-sm">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-3">
          <div class="text-center text-lg-start">
            <RouterLink to="/" class="text-secondary text-decoration-none fs-4">VueFashion</RouterLink>
          </div>
        </div>
        <div class="col-md-8 col-lg-6 py-md-2 py-lg-0">
          <ul class="list-unstyled d-flex m-0 p-0">
            <li class="me-1"><RouterLink to="/" class="text-secondary text-decoration-none px-3 py-1">Home</RouterLink></li>
            <li class="me-1"><RouterLink to="/products" class="text-secondary text-decoration-none px-3 py-1">Products</RouterLink></li>
          </ul>
        </div>
        <div class="col-md-4 col-lg-3 py-md-2 py-lg-0">
          <div class="d-flex justify-content-end py-lg-2">
            <div class="dropdown d-inline-flex d-sm-none">
              <button type="button" class="btn border-0 shadow-none" data-bs-toggle="collapse" data-bs-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
                <span class="icon"><IconBar /></span>
              </button>
            </div>
            <div class="dropdown d-inline-flex">
              <button type="button" class="btn border-0 position-relative" data-bs-toggle="offcanvas" data-bs-target="#minicart" aria-controls="offcanvasRight">
                  <span class="icon">
                    <IconCart />
                  </span>
                  <span class="small position-absolute d-inline-flex p-2 align-items-center translate-middle bg-secondary text-light rounded-circle" style="font-size:10px;height:20px;width:20px;left:35px">9+</span>
              </button>
              
            </div>
            
            <div class="dropdown d-inline-flex">
              <button type="button" class="btn border-0" data-bs-toggle="dropdown" aria-expanded="false">
                <span class="icon">
                  <Iconuser />
                </span>
              </button>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Login</a></li>
                <li><a class="dropdown-item" href="#">Register</a></li>
                <li><a class="dropdown-item" href="#">Logout</a></li>
              </ul>
            </div>
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
        <p>Lorem ipsum dolor sit amet.</p>
      </div>
      <div class="offcanvas-footer px-4 py-3">
        Lorem ipsum dolor, sit amet consectetur
      </div>
    </div>
      
  </header>

  <RouterView />
 
</template>

<style scoped>
</style>
