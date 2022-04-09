<template>
<!-- SECTION SUBSCRIPTION -->
<section>
    <div class="container p-5 mb-5">
        <!-- SUBSCRIPTION TEXT -->
        <div class="row text-center">
            <div class="col">
                <h2 class="fw-bold mb-4">Our rates for developer from landrick team</h2>
                <p class="text-secondary mb-5">Start working with <span class="my-blue-text fw-bold">Landrick</span> that can provide everthing you need to generate <br> awareness, drive traffic, connect.</p>
            </div>
        </div>
        <!-- /SUBSCRIPTION TEXT -->

        <!-- SUBSCRIPTION CARD PLANS -->
        <div class="row mb-5">
            <div class="col-4" v-for="(card, index) in subscriptionPlans" :key="index">
                <div class="card p-4">
                    <div class="card-body">
                        <span id="plans" class="d-inline-block fw-bold my-blue-text my-alice-blue-bg border rounded-pill mb-3">{{ card.planType }}</span>
                        <h2 class="card-text fw-bold">{{ card.price }}</h2>
                        <p class="card-text text-secondary">Per Month</p>
                        <p class="card-text text-secondary">{{ card.text }}</p>
                        <hr>
                        <ul class="card-text p-0 mb-4">
                            <li class="d-flex align-items-center text-secondary fw-bold mb-2" v-for="(element, index) in propertiesPlan" :key="index"><span class="fas fa-check my-fa-check-blue me-2"></span>{{ element.property }}</li>
                        </ul>
                        <div class="card-text d-flex text-center mb-3">
                            <a class="col-12 me-3 text-decoration-none p-2 text-white my-blue-bg rounded shadow-lg" href="#">Buy Now</a>
                        </div>
                        <span class="card-text text-secondary">*No credit card required</span>
                    </div>
                </div>
            </div>
        </div>
        <!-- /SUBSCRIPTION CARD PLANS -->

        <!-- SUBMIT -->
        <div class="row text-center pt-5 mb-5">
            <div class="col-12">
                <div class="wrapper">
                    <h2 class="fw-bold mb-4">Want to be among the first to find out?</h2>
                    <p class="text-secondary mb-4">Start working with <span class="my-blue-text fw-bold">Landrick</span> that can provide everthing you need to generate <br> awareness, drive traffic, connect.</p>
                    <div class="input-group">
                        <input type="email" class="form-control" placeholder="Email Address">
                        <button id="btn-getStarted" class="btn text-white btn-outline-secondary" type="sumbmit">Get Started</button>
                    </div>
                </div>
            </div>
        </div>
        <!-- /SUBMIT -->
    </div>
</section>
<!-- SECTION SUBSCRIPTION CARDS -->
</template>


<script>
export default {
    name:'SubscriptionCardsSection',


    data: function(){
        return{
            subscriptionPlans:[
                {
                    planType:'Basic',
                    price: '$9.00',
                    text: 'All the basics for businesses that are just getting started'
                },

                {
                    planType:'Business',
                    price: '$39.00',
                    text: 'Better for growing businesses that want more customers.'
                },

                {
                    planType:'Enterprise',
                    price: '$79.00',
                    text: 'Advanced features for pros who need more customization.'
                }
            ],

            propertiesPlan:[
                {
                    property: 'Full Access'
                },

                {
                    property: 'Enhanced Security'
                },

                {
                    property: 'Source Files'
                },

                {
                    property: '1 Domain Free'
                },

                {
                    property: 'Enhanced Security'
                },
            ]
        }
    }
}
</script>


<style lang="scss">

    div.card{
        border-bottom: 4px solid rgb(150, 150, 150);
        border-radius: 15px ;

        span#plans{
            padding: .5rem 1.5rem;
        }
    }

    button#btn-getStarted{
        background-color: #2F55D4
    }
</style>