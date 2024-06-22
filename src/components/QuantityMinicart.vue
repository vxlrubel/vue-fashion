<template>
    <span>Quantity: </span>
    <div class="quantity d-inline-flex align-items-center">
        <button class="btn border-0 rounded-0 p-2" :disabled="quantity <= 1" @click.prevent="decrement">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                <path d="M432 256c0 17.7-14.3 32-32 32L48 288c-17.7 0-32-14.3-32-32s14.3-32 32-32l352 0c17.7 0 32 14.3 32 32z"/>
            </svg>
        </button>
        <input type="number" :value="quantity" @input="updateQuantity" step="1" max="50" min="1">
        <button class="btn border-0 rounded-0 p-2" :disabled="quantity >= 50" @click.prevent="increment">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                <path d="M256 80c0-17.7-14.3-32-32-32s-32 14.3-32 32V224H48c-17.7 0-32 14.3-32 32s14.3 32 32 32H192V432c0 17.7 14.3 32 32 32s32-14.3 32-32V288H400c17.7 0 32-14.3 32-32s-14.3-32-32-32H256V80z"/>
            </svg>
        </button>
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
    .quantity .btn{
        background-color:#f1f2f6;
    }
    .quantity .btn:hover{
        background-color:#dfe4ea;
    }
    .quantity .btn,
    .quantity .btn,
    .quantity input{
        display: inline-flex;
        justify-content: center;
        align-items: center;
        height: 28px;
        width: 28px;;
    }
    .quantity input{
        border: 0;
        border-left: 1px solid #dee2e6;
        border-right: 1px solid #dee2e6;
        width: 50px;
        box-shadow: none !important;
        outline: 0;
        text-align: center;
    }
    .quantity input[type="number"]::-webkit-outer-spin-button,
    .quantity input[type="number"]::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }
    .quantity input[type="number"] {
        -moz-appearance: textfield;
    }

</style>
