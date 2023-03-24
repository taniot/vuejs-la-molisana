<script>
import CardElement from './CardElement.vue';

export default {
    name: 'DiscountList',
    components: {
        CardElement
    },
    data() {
        return {
            products: [
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
                    titolo: "N.4 Spaghetto Quadrato Bucato",
                    tipo: "lunga",
                    cottura: 6,
                },
                {
                    src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
                    titolo: "N.5 Fettuccine",
                    tipo: "lunga",
                    cottura: 13,
                },
            
            ]
        }
    }
}
</script>

<template>
    <section>
        <h2>Lista Discount</h2>
        <div class="container">
            <div class="discounts">
                <!-- <div class="product" v-for="product in products">
                    <div><img :src="product.src"></div>
                    <h3>{{ product.titolo }}</h3>
                </div> -->
                <CardElement 
                    class="discount" 
                    v-for="product in products" 
                    :img="product.src"
                    :title="product.titolo"
                    />
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

section {
    @include bgImage('../assets/img/bg-products.jpg');
    padding: 3.75rem;
}

h2 {
    text-align: center;
    margin-bottom: 20px;
}

.discounts {
    display: flex;
    flex-wrap: wrap;

    .discount {
        // flex-basis: calc(100% / 4);
        width: 50%;
        border: $secondary-color 2px solid;
        background-color: yellow;
        padding: 20px;
        
  

        :deep(h3) {
            color: $primary-color;
            text-align: center;
        }
    }
}
</style>