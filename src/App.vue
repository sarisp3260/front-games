<template>
  <header>
    <div class="container">
      <div class="top_nav">
        <figure>
          <img src="./assets/Logos/logoWhite.png" alt="logo">
        </figure>
        <h1>Game Load</h1>
        <div class="menu">
          <ul>
            <li><a href="#">¿Qienes Somos?</a></li>
            <li><a href="#">Registrarse</a></li>
            <li><a href="#">Iniciar sesión</a></li>
          </ul>
        </div>
      </div>
      <div class="bottom_nav">
        <ul>
          <li><a href="#">Inicio</a></li>
          <li><a href="#">Playstation</a></li>
          <li><a href="#">Xbox</a></li>
          <li><a href="#">Nintendo</a></li>
          <li><a href="#">Acesorios</a></li>
          <li ><a  class="carrito" href="#">$0 <i class="fas fa-shopping-cart"></i></a></li>

        </ul>
      </div>
    </div>
  </header>
  <main id="app">
    <section class="products">
      <Cards v-for="product in products" 
      :key="product.title" 
      :product="product"/> 
    </section>
  </main>
  
  <footer>
    <div class="all-footer">
        <figure class="logo-footer">
            <img src="./assets/Logos/logoWhite.png" alt="Logo">
        </figure>
        <div class="info">
          <ul>
            <li class="big"><a href="#">Tienda</a></li>
            <li><a href="#">Mas reciente</a></li>
            <li><a href="#">Accesorios premium</a></li>
            <li><a href="#">Suscripción</a></li>
          </ul>
        </div>
        <div class="servicio">
          <ul>
            <li class="big"><a href="#">Servicio al cliente</a></li>
            <li><a href="#">pedidos@gamesload.com</a></li>
            <li><a href="#">Cll 78 #40-5 Bogotá, Colombia</a></li>
            <li><a href="#">(+57)369 874 21 45  -  478 214 21</a></li>
          </ul>
        </div>
        <div class="socilamedia">
          <ul class="smedia">
            <li>Follow us</li>
            <li><i id="facebook" class="fab fa-facebook"></i></li>
            <li><i id="youtube" class="fab fa-youtube"></i></li>
            <li><i id="insta" class="fab fa-instagram"></i></li>
          </ul>
        </div>
      </div>
      <div class="sponsor">
      
        <img src="./assets/footer/textonly.png" alt="">
        <img src="./assets/footer/logops.png" alt="">
        <img src="./assets/footer/logonswitch.png" alt="">
        <img src="./assets/footer/logoxbox.png" alt="">
    
      </div>
  </footer>
</template>

<script>

import Cards from './components/Cards.vue'

export default {
  name: 'App',
  components: { Cards },
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
:root{--primary-color: #0D0D0D;--palette-pink: #EE05F2 ;--heavy-blue: #0378A6; --medium-blue: #04ADBF;--light-blue: #04D9C4;	--secundary-color: #fff; --size: 18px;}
*{margin: 0; padding: 0;box-sizing: border-box;}
#app 
{font-family:'Roboto', sans-serif;}

figure img
{margin: 0 20px; height: 40px; vertical-align: bottom;}
.container .top_nav
{width: 100%;height: 65px;background: var(--heavy-blue);padding: 0 50px;display: flex;justify-content: space-between;align-items: center; color: var(--secundary-color);}
.container .top_nav {display: flex;align-items: center;}
.container .top_nav .logo p
{font-size: 24px;display: inline;font-weight: bold;color: var(--secundary-color);margin-right: 25px;padding-bottom: 10px;}
.container .top_nav .logo img{width: 40px;}
.container .top_nav .menu ul{display: flex;}
.container .top_nav .menu ul li{ margin: 0 12px; list-style: none;}
.container .top_nav .menu ul li:last-child
{background:var(--light-blue);margin-right: 0;border-radius: 2px;text-transform: uppercase; font-weight: 700;}
.container .top_nav .menu ul li:hover:last-child
{background: var(--palette-pink)}
.container .top_nav .menu ul li a
{display: block;padding: 8px 10px;color: var(--secundary-color);text-decoration: none;}
.container .top_nav .menu ul li:last-child a
{color: var(--secundary-color);}
.container .bottom_nav
{width: 100%;background:var(--medium-blue);height: 45px;padding: 0 100px;}
.container .bottom_nav ul
{width: 100%;height: 45px;list-style: none;display: flex;justify-content: space-between;align-items: center; font-weight: 700;}
.container .bottom_nav ul li a
{color: var(--secundary-color);font-size: 16px; text-decoration: none;}
.container .carrito
{background: var(--heavy-blue); padding: 5px 10px; border-radius: 20px;}
.container .bottom_nav ul li .carrito:hover
{border: none; background: #494949; color: #f9f9f9;}
/*-------------------------------------------------------------------------------- */
footer 
{ background: var(--primary-color); color:var(--secundary-color); width: 100%; height: auto; position: absolute; bottom: 0; padding: 20px 0; align-items: center;}
.all-footer
{margin: 0 auto;grid-gap: 80px; display: flex;  align-items: center; justify-content: center;}
footer img
{ height: 50px; margin: 0 20px; vertical-align: bottom;}
footer ul 
{display: inline-table; list-style: none; text-transform: uppercase;font-weight: 500;}
.info a
{text-decoration: none; color: var(--secundary-color)}
footer .socilamedia ul
{ color: var(--secundary-color); display: flex; list-style: none;align-items: center;}
.socilamedia ul li
{padding: 0 20px; font-size: var(--size); text-transform: uppercase;font-weight: 500; }
.socilamedia ul li i
{font-size: 30px; cursor: pointer;}
.servicio ul li a{text-decoration: none; color: var(--secundary-color);}
.sponsor
{display: flex; padding: 30px 40px 10px; justify-content: center;}
.sponsor img{align-items: center;}
main 
{width: 100vw;overflow: hidden;display: flex;justify-content: center;align-items: center;}
.products {display: flex ;max-width: 1280px;padding: 25px;margin: 0 auto;}
</style>
