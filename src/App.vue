<script setup>
  import { RouterLink, RouterView } from 'vue-router';
  import IconBar from './components/icons/IconBar.vue';
  import MinicartIcon from './components/MinicartIcon.vue';
  import UserDropdown from './components/UserDropdown.vue';
  import Minicart from './components/Minicart.vue';
  import MobileMenu from './components/MobileMenu.vue';
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
    
    <MobileMenu/>
    
    <Minicart/>

      
  </header>

  <RouterView />
 
</template>

<style scoped>
</style>
