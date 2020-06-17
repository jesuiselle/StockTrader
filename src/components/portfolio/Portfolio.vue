<template>
    <div>
        <app-stock-portfolio v-for="stock in stocks" :stock="stock"></app-stock-portfolio>
    </div>
</template>

<script>
    import {mapGetters} from 'vuex';
    import Stock from '../portfolio/Stock.vue';

    export default {
        computed: {
            ...mapGetters({
                stocks: 'stockPortfolio'
            })
        },
        components: {
            appStockPortfolio: Stock
        }
    }
</script>
