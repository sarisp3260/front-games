<template>
    <div id="User">
        <h2 class="nameCataloge">Bienvenido <span> {{username}}, </span> , estas son las mejores recomendaciones para ti</h2>
        <section class="products">
        <Cards v-for="product in products" 
        :key="product.title" 
        :product="product"/> 
        </section>
    </div>
</template>

<script>
import Cards from './Cards.vue'

    export default {
        name: "User",
        components: { Cards },
        
        data:function(){
            return {
                username: "none",
                products: [
        {
          title: 'Batman',
          price: '$20.000 COP',
          category: 'Juegos',
      //     src: '../assets/logo.png'
        },
        {
          title: 'Fifa21',
          price: '$20.000 COP',
          category: 'Juegos',
      //     src: require('./assets/products/fifa21.jpeg')
        },
        {
          title: 'Marvel spider man',
          price: '$20.000 COP',
          category: 'Juegos',
      //     src: require('./assets/products/marvel-s-spider-man.jpg')
        },
        {
          title: 'GTA 5',
          price: '$20.000 COP',
          category: 'Juegos',
      //     src: require('./assets/products/marvel-s-spider-man.jpg')
        }
      ]
            }
        },
        
        created: function(){
            this.username = this.$route.params.username
        }
    }
</script>


<style>
span {
    color: var(--heavy-blue);
}
</style>