<template>
    <div class="quantity d-inline-flex align-items-center">
        <button class="btn border-0" :disabled="quantity <= 1" @click.prevent="decrement">-</button>
        <input type="number" :value="quantity" @input="updateQuantity" step="1" max="50" min="1">
        <button class="btn border-0" :disabled="quantity >= 50" @click.prevent="increment">+</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quantity: 1
            };
        },
        methods: {
            increment() {
                if (this.quantity < 50) {
                    this.quantity++;
                }
            },
            decrement() {
                if (this.quantity > 1) {
                    this.quantity--;
                }
            },
            updateQuantity(event) {
                const value = parseInt(event.target.value, 10);
                if (!isNaN(value) && value >= 1 && value <= 50) {
                    this.quantity = value;
                }
            }
        }
    };
</script>

<style scoped>
    .quantity{
        border: 1px solid #dee2e6;
    }
    .quantity .btn,
    .quantity input{
        display: inline-flex;
        justify-content: center;
        align-items: center;
        height: 28px;
        width: 28px;
    }
    .quantity input{
        border: 0;
        border-left: 1px solid #dee2e6;
        border-right: 1px solid #dee2e6;
        width: 50px;
    }
</style>
