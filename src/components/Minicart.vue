<template>
    <div class="offcanvas offcanvas-end" tabindex="-1" id="minicart" aria-labelledby="shoppingCartTitle">
      <div class="offcanvas-header px-4">
        <div class="d-flex" id="shoppingCartTitle">
          <h4 class="fs-5 m-0">Shopping Cart</h4>
          <div class="ms-2">items-12</div>
        </div>
        <button type="button" class="btn-close shadow-none" data-bs-dismiss="offcanvas" aria-label="Close"></button>
      </div>
      <div class="offcanvas-body px-4">
        <div class="d-flex">
            <div class="me-2" style="width:50px;height:60px;">
              <img src="https://img.freepik.com/free-photo/woman-dress_1303-3764.jpg?t=st=1719081743~exp=1719085343~hmac=49052437edf9fa5911ba79745e443c5396008c802ec4bcab3b4e5a0f937930a6&w=360" class="w-100 h-100 object-fit-cover" alt="product image">
            </div>
            <div style="width: calc(100% - calc(50px + .5rem));">
              <div class="d-flex align-items-center">
                <div style="width: calc(100% - calc(20px + .5rem));">
                  <a href="javascript:void(0)" class="d-block text-decoration-none text-body text-truncate">Ethereal Elegance KurtiEthereal Elegance KurtiEthereal Elegance Kurti</a>
                </div>
                <button class="btn btn-sm p-0 ms-2 border-0" style="width: 20px;">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="var(--vf-color-red)" viewBox="0 0 512 512"><path d="M256 48a208 208 0 1 1 0 416 208 208 0 1 1 0-416zm0 464A256 256 0 1 0 256 0a256 256 0 1 0 0 512zM175 175c-9.4 9.4-9.4 24.6 0 33.9l47 47-47 47c-9.4 9.4-9.4 24.6 0 33.9s24.6 9.4 33.9 0l47-47 47 47c9.4 9.4 24.6 9.4 33.9 0s9.4-24.6 0-33.9l-47-47 47-47c9.4-9.4 9.4-24.6 0-33.9s-24.6-9.4-33.9 0l-47 47-47-47c-9.4-9.4-24.6-9.4-33.9 0z"/></svg>
                </button>
              </div>

              <div class="price">
                Price: <span class="text-primary">$25.00</span> || <span class="text-danger text-decoration-line-through">$29.00</span> 
              </div>

              
              <QuantityMinicart/>
              
            </div>
        </div>
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
</template>

<script setup>
  import QuantityMinicart from './QuantityMinicart.vue';
</script>


<style lang="scss" scoped>

</style>