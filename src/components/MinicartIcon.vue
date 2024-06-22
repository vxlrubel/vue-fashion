
<script setup>
    import IconCart from './icons/IconCart.vue';
</script>

<template>
    <div class="dropdown d-inline-flex">
        <button type="button" class="btn border-0 position-relative" data-bs-toggle="offcanvas" data-bs-target="#minicart" aria-controls="offcanvasRight">
            <span class="icon">
                <IconCart />
            </span>
            <span class="small position-absolute d-inline-flex p-2 align-items-center translate-middle bg-secondary text-light rounded-circle" style="font-size:10px;height:20px;width:20px;left:35px">9+</span>
        </button>
    </div>
</template>


<style lang="scss" scoped>

</style>