<template>
    <div class="container">
        <div class="row pt-5">
            <h2 class="display-2">Products</h2>
        </div>
        <div class="row justify-content-center gap-3">
            <Card v-for="(product, id) in products" :key="id">
            <template #cardHeader>
            <img class="img-fluid" :src="product.profile" :alt="product.productName" loading="lazy">
            </template>
            <template #cardBody>
            <h5>{{ product.productName }}</h5>
            <h6>Price: R{{ product.price }}</h6>
            <p>{{ product.description }}</p>
            <p>{{ product.status }}</p>
            </template>
        </Card>
        </div>        
    </div>
  </template>
  
  <script>
    import Card from './Card.vue'

  export default {
    name: 'ProductsComp',
    components: {Card},
    data() {
        return {
            products : [
                {
                    id: "1",
                    productName: "Black Coffee",
                    description: "Special Houseblend of Straight black Coffee.",
                    price: 25,
                    status: "In Stock",
                    profile: "https://achar1f.github.io/projectimages/kafenioimages/black-coffee.jpg" 
                },
                {
                    id: "2",
                    productName: "Cappucino",
                    description: "Our special blend crafted specifically for Cappucino.",
                    price: 28,
                    status: "In Stock",
                    profile: "https://achar1f.github.io/projectimages/kafenioimages/red-cappucino.jpg"
                },
                {
                    id: "3",
                    productName: "Single Esspresso",
                    description: "Single Shot of our special homeblend espresso.",
                    price: 10,
                    status: "In Stock",
                    profile: "https://achar1f.github.io/projectimages/kafenioimages/single-expresso.jpg" 
                },
                {
                    id: "4",
                    productName: "Double Esspresso",
                    description: "Double shot of our special homeblend esspresso.",
                    price: 18,
                    status: "In Stock",
                    profile: "https://achar1f.github.io/projectimages/kafenioimages/double-expresso.jpg" 
                },
                {
                    id: "5",
                    productName: "Hot Choc",
                    description: "Rich and Creamy Hot Chocolate Topped with Cream.",
                    price: 45,
                    status: "In Stock",
                    profile: "https://achar1f.github.io/projectimages/kafenioimages/hot-chocolate.jpg" 
                },
                {
                    id: "6",
                    productName: "Choc Milkshake",
                    description: "Shake with chocolate, cream and marshmallows.",
                    price: 40,
                    status: "In Stock",
                    profile: "https://achar1f.github.io/projectimages/kafenioimages/Chocolate-milkshake.jpg" 
                }
            ]
        }
    }
  }
  </script>
  

  <style scoped>
    .card {
        background-color: #DAA06D;
    }
  </style>
  