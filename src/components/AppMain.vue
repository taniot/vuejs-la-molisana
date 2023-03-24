<script>
import ProductsList from './ProductsList.vue';
import DiscountList from './DiscountList.vue';
export default {
    name:'AppMain',
    components: {
        ProductsList,
        DiscountList
    }
}
</script>

<template>
    <main>
        <!-- Lista prodotti -->

        <ProductsList />
        <DiscountList />
    </main>
</template>