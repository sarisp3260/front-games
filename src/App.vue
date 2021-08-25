<template>

  <header>
    <Heading />
    <SubNav />
  </header>

  <main id="app">
    <div class="container"> 
    </div>
    <section class="products">
      <Cards v-for="product in products" 
      :key="product.title" 
      :product="product"/> 
    </section>
  </main>
  <SingUp />
  <Ingreso />
  <Button title="Damion es mion" class="optional"/>

  <footer>
    <Footer />
    
  </footer>
</template>

<script>

import Cards from './components/Cards.vue'
import Button from './components/Button.vue'
import Ingreso from './components/Ingreso.vue'
import SingUp from './components/SingUp.vue'
import SubNav from './components/SubNav.vue'
import Heading from './components/Heading.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: { Cards, Button, Ingreso, SingUp, Heading, SubNav, Footer },
  data(){
    return{
    products: [
        {
          title: 'Batman',
          price: '$20.000 COP',
          category: 'Juegos',
          src: '../assets/logo.png'
        },
        {
          title: 'Fifa21',
          price: '$20.000 COP',
          category: 'Juegos',
          src: require('./assets/products/fifa21.jpeg')
        },
        {
          title: 'Marvel spider man',
          price: '$20.000 COP',
          category: 'Juegos',
          src: require('./assets/products/marvel-s-spider-man.jpg')
        },
        {
          title: 'GTA 5',
          price: '$20.000 COP',
          category: 'Juegos',
          src: require('./assets/products/marvel-s-spider-man.jpg')
        }
      ]
    }
  }

}


</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200;300;400;500;600;700&family=Roboto:wght@100;300;400;500;900&display=swap');
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
:root {
  --primary-color: #0D0D0D;
  --palette-pink: #EE05F2 ;
  --heavy-blue: #0378A6;
  --medium-blue: #04ADBF;
  --light-blue: #04D9C4;
  --secundary-color: #fff;
  --size: 18px;
  --ff-primary: 'Roboto', sans-serif;
  --ff-secondary: 'Oswald', sans-serif;
  --transition: all 0.3s linear;
  --spacing: 0.1rem;
  --radius: 0.25rem;
  --light-shadow: 0 5px 15px rgba();
  --dark-shadow: 0 5px 15px rgba();
  --max-width: 1170px;
  --fixed-width: 620px;
  }
*{
  box-sizing: border-box;
}
#app {
  font-family:var(--ff-primary);
}
figure img {
  margin: 0 20px;
  height: 40px;
  vertical-align: bottom;
}
/*-------------------------------------------------------------------------------- */
footer {
  bottom: 0;
  position: fixed;
  width: 100%;
}
main 
{width: 100vw;overflow: hidden;display: flex;justify-content: center;align-items: center;}
.products {display: flex ;max-width: 1280px;padding: 25px;margin: 0 auto;}
</style>
