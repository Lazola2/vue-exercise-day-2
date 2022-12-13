<template>
    <div v-for="item in items" :key="item">
        <div class="card mb-5 text-white" style="width: 18rem;">
            <img :src=item.imageLink class="card-img-top" :alt="item.brand" loading="lazy">
            <div class="card-body">
                <div class="name-and-price d-flex justify-content-between">
                    <h5 class="card-title">{{item.brand}}</h5>
                    <h5 class="card-title">R{{item.price}}</h5>
                </div>
                
                <p class="card-text text-center">{{item.specifications.toString()}}</p>
                <div class="button-holder d-flex justify-content-center">
                    <button class="btn add-btn w-50" v-on:click='greet'>Add</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductContainer',
    data() {
        return {
            items: [
                {
                    id: 1,
                    brand: 'Lenovo',
                    price: 9000,
                    specifications: ['Lenovo ThinkPad', 'Intel Core i5 Processor', '8GB RAM', '500GB HDD', 'Windows 10 Pro'],
                    color: 'Silver',
                    imageLink: 'https://i.postimg.cc/Jzd7CVzQ/Lenovo-thinkpad.webp'
                },
            ]
        }
    },
    methods: {
        greet: function(event){
            event.preventDefault();
            alert('Hello there');
        }
    }
}
</script>
