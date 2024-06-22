<script setup>
    import Iconuser from './icons/IconUser.vue';
</script>

<template>
    <div class="dropdown d-inline-flex">
        <button type="button" class="btn border-0" data-bs-toggle="dropdown" aria-expanded="false">
            <span class="icon">
                <Iconuser />
            </span>
        </button>
        <ul class="dropdown-menu p-2 shadow-sm">
            <li><a class="dropdown-item" href="javascript:void(0)">Login</a></li>
            <li><a class="dropdown-item" href="javascript:void(0)">Register</a></li>
            <li><a class="dropdown-item" href="javascript:void(0)">Logout</a></li>
        </ul>
    </div>
</template>



<style lang="scss" scoped>

</style>