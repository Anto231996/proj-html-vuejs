<template>
    <!-- FOOTER BOTTOM -->
    <section class="container px-5">
        <div class="row py-4">
            <!-- COPYRIGHT -->
            <div class="col">
                <p class="text-secondary">© 2020 Landrick. Design with <i class="fa fa-heart text-danger"></i> by Shreethemes</p>
            </div>
            <!-- /COPYRIGHT -->
            <!-- PAYMENT CARD -->
            <div class="col d-flex justify-content-end">
                <img class="ms-2" v-for="(card, index) in paymentCards" :key="index" :src="require(`../assets/img/${card.logo}`)" :alt="card.name">
            </div>
            <!-- /PAYMENT CARD -->
        </div>
    </section>
    <!-- /FOOTER BOTTOM -->
</template>


<script>
export default {

    name: 'FooterBottom',

    data: function () {
        return{

            /* LISTA DELLE METODI DI PAGAMENTO ACCETTATI */
            paymentCards:[
                {
                    name:'American-Ex card',
                    logo:'american-ex.png',
                },

                {
                    name:'Discover card',
                    logo:'discover.png',
                },

                {
                    name:'Master-Card card',
                    logo:'master-card.png',
                },

                {
                    name:'PayPal card',
                    logo:'paypal.png',
                },

                {
                    name:'Visa card',
                    logo:'visa.png',
                }
            ]
        }
    }
}
</script>


<style lang="scss" scoped>
    img{
        height: 25px;
    }
</style>