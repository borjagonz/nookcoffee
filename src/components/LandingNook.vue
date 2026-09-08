<template>
    <div class="landing">
<nav
  class="navbar"
  :class="{ scrolled: isScrolled }"
>
  <a href="#home" @click="closeMenu">
    <img class="logo" src="../icons/nook-icon.svg" alt="Nook Coffee">
  </a>

  <!-- Botón hamburguesa -->
  <button
    class="hamburger"
    @click="toggleMenu"
    :class="{ active: menuOpen }"
  >
    <span></span>
    <span></span>
    <span></span>
  </button>

  <!-- Menú -->
  <div
    class="navbuttons"
    :class="{ open: menuOpen }"
  >
    <a class="navbtn" href="#menu" @click="closeMenu">Menu</a>
    <a class="navbtn" href="#location" @click="closeMenu">Encuéntranos</a>
    <a class="navbtn" href="#contact" @click="closeMenu">Contacto</a>

    <a
      href="https://www.instagram.com/nook___coffee/?hl=es"
      target="_blank"
      @click="closeMenu"
    >
      <img
        class="ig-icon"
        src="../icons/instagram-icon.svg"
        alt=""
      >
    </a>
  </div>
</nav>
<header class="header" id="home">

    <div
        class="header-slider"
    >
<div
    ref="track"
    class="header-track"
    :style="{ transform: `translateX(-${offset}px)` }"
>
            <div
                v-for="(image, index) in loopImages"
                :key="index"
                class="header-slide"
            >
                <img :src="image" alt="">
            </div>
        </div>

    </div>
    <p class="header-avantitle">GOOD COFFEE, FEELS LIKE HOME</p>
    <h1>WELCOME</h1>
<h3
  class="nook-coffee"
  :class="{ blue: isOnLightSection }"
>
  NOOK COFFEE
</h3>
<div class="services">
    <div class="dog-friendly"><img class="dog-icon" src="../icons/dog-icon.svg" alt=""><span class="service">Dog Friendly</span></div>
    <div class="dog-friendly"><img class="dog-icon" src="../icons/wifi-icon.svg" alt=""><span class="service">Free Wi-Fi</span></div>
    <div class="dog-friendly"><img class="dog-icon" src="../icons/laptop-icon.svg" alt=""><span class="service">Laptop Friendly</span></div>
    <div class="dog-friendly"><img class="dog-icon" src="../icons/creditcard-icon.svg" alt=""><span class="service">Credit Card Accepted</span></div>
</div>
        

</header>
<section class="about">
    <p>Nook Coffee es un rincón donde el café de especialidad, la buena comida y un ambiente acogedor se encuentran. Creamos un espacio cercano y auténtico para disfrutar de desayunos, brunch y momentos que merecen una pausa.
</p>
</section>
        <section class="menu" id="menu">
        <h1>MENU</h1>
        <h2>Nook Coffee</h2>
        <ul class="menu-list">
            <li class="menu-item"><span>ESPRESSO</span><span class="price">1.80</span></li>
            <li class="menu-item"><span>ESPRESSO DOBLE</span><span class="price">2</span></li>
            <li class="menu-item"><span>CORTADO</span><span class="price">2</span></li>
            <li class="menu-item"><span>FLAT WHITE</span><span class="price">3</span></li>
            <li class="menu-item"><span>LATTE</span><span class="price">2.40</span></li>
            <li class="menu-item"><span>CAPUCCINO</span><span class="price">3</span></li>
            <li class="menu-item"><span>LATTE XL</span><span class="price">3.20</span></li>
            <li class="menu-item"><span>AMERICANO</span><span class="price">2.50</span></li>
            <li class="menu-item"><span>BATCH BREW</span><span class="price">2.60</span></li>
            <li class="menu-item"><span>MACHA LATTE</span><span class="price">3.50</span></li>
            <li class="menu-item"><span>CHAI LATTE</span><span class="price">3.50</span></li>
            <li class="menu-item"><span>ICED LATTE</span><span class="price">4</span></li>
            <li class="menu-item"><span>ICED MATCHA</span><span class="price">4</span></li>
            <li class="menu-item"><span>ICED CHAI</span><span class="price">4</span></li>
        </ul>
        </section>
        <section class="menu-2">
        <ul class="menu-list">
            <li class="menu-item2"><span>PAN DE MASA DE MADRE<p class="sub-item">CON MANTEQUILLA Y MERMELADA CASERA</p></span><span class="price">1.80</span></li>
            <li class="menu-item2"><span>TOSTADA VERDE<p class="sub-item">HUMUS DE EDAMAME Y ANACARDO, AGUACATE, DUKKAH</p></span><span class="price">1.80</span></li>
            <li class="menu-item2"><span>TOSTADA MATÓ Y CHERRIES CONFITADOS</span><span class="price">4</span></li>
            <li class="menu-item2"><span>MELT DE PATÉ<p class="sub-item">TOMATES SECOS, SHITAKES Y QUESO EMMENTAL</p></span><span class="price">1.80</span></li>
            <li class="menu-item2"><span>KIMCHEESE<p class="sub-item">KIMCHI, COMTÉ, KALE</p></span><span class="price">1.80</span></li>
            <li class="menu-item2"><span>MELT VEGANO<p class="sub-item">CALABACÍN, PATATAS, ESPINACA, CREMA DE ALCACHOFA</p></span><span class="price">1.80</span></li>
            <li class="menu-item2"><span>DANISH BREAKFAST<p class="sub-item">PAN INTEGRAL DE PISTACCIO, HUEVO PASADO POR AGUA, CHEDDAR INGLÉS, MANTEQUILLA, MERMELADA CASERA</p></span><span class="price">1.80</span></li>
            <li class="menu-item2"><span>HUEVOS A LA PLANCHA CON JAMÓN</span><span class="price">4</span></li>
            <li class="menu-item2"><span>FRENCH TOAST<p class="sub-item">CREMA MASCARPONE, SALTED CARAMEL, PLÁTANO FLAMBEADO</p></span><span class="price">1.80</span></li>
            <li class="menu-item2"><span>YOGUR CON GRANOLA<p class="sub-item">YOGUR CON GRANOLA CASERA, COMPOTA DE FRUTA, RALLADURA DE LIMA, MENTA</p></span><span class="price">1.80</span></li>
            <li class="menu-item2"><span>PORRIDGE<p class="sub-item">AVENA CALIENTE, COMPOTA DE FRUA, NUECES CARAMELIZADAS</p></span><span class="price">1.80</span></li>
        </ul>        
    </section>
<section class="location" id="location">

    <div class="location-content">

        <div class="location-info">

            <p class="location-tag">
                COME VISIT US
            </p>

            <h1>
                SEE YOU HERE
            </h1>

            <div class="location-address">
                Marià Cubí, 13 bis<br>
                08006 Barcelona
            </div>

            <div class="location-hours">

                <div class="hours-row">
                    <span>MON — FRI</span>
                    <span>08:00 — 18:00</span>
                </div>

                <div class="hours-row">
                    <span>SAT — SUN</span>
                    <span>09:00 — 18:00</span>
                </div>

            </div>

            <a
                class="directions-btn"
                href="https://maps.google.com/?q=Nook+Coffee+Barcelona"
                target="_blank"
            >
                GET DIRECTIONS
            </a>

        </div>

        <div class="location-map">

            <iframe
                class="mapa"
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2992.853321748978!2d2.1485583121612555!3d41.398991671178585!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x12a4a357a67107ef%3A0x6ce649e7628e8610!2sNook%20Coffee!5e0!3m2!1ses!2ses!4v1782143820285!5m2!1ses!2ses"
                allowfullscreen=""
                loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"
            ></iframe>

        </div>

    </div>

</section>
<section class="contact" id="contact">

    <p class="contact-tag">
        LET'S TALK
    </p>

    <h1>
        SAY HELLO
    </h1>

    <p class="contact-description">
        Questions, collaborations or just fancy a chat?
    </p>

    <form class="contact-form">

        <input
            type="text"
            placeholder="Your name"
        >

        <input
            type="email"
            placeholder="Your email"
        >

        <textarea
            rows="5"
            placeholder="Your message"
        ></textarea>

        <button type="submit">
            SEND MESSAGE
        </button>

    </form>

</section>
<footer class="footer">
    <span>© 2026 Nook Cooffee. All rights reserved</span>
    <a href="">Legal Notice & Privacy Policy</a>
    <a href="">Cookies Policy</a>
</footer>
    </div>
    <ScrollToTopButton></ScrollToTopButton>
</template>

<script setup>
import ScrollToTopButton from './ScrollToTopButton.vue'
import { ref, onMounted, onBeforeUnmount } from 'vue'

import img1 from '../assets/img-1.jpg'
import img2 from '../assets/img-2.jpg'
import img3 from '../assets/img-3.jpg'
import img4 from '../assets/img-4.jpg'
import img5 from '../assets/img-5.jpg'
import img6 from '../assets/img-6.jpg'
import img7 from '../assets/img-7.jpg'
import img8 from '../assets/img-8.jpg'
import img9 from '../assets/img-9.jpg'
import img10 from '../assets/img-10.jpg'
import img11 from '../assets/img-11.jpg'
import img12 from '../assets/img-12.jpg'
import img13 from '../assets/img-13.jpg'

const isScrolled = ref(false)
const isOnLightSection = ref(false)

const images = [
  img1,
  img2,
  img3,
  img4,
  img5,
  img6,
  img7,
  img8,
  img9,
  img10,
  img11,
  img12,
  img13
]

const loopImages = [...images, ...images]

const track = ref(null)
const offset = ref(0)

let animationFrame = null
let resetPoint = 0

const moveSlider = () => {
  offset.value += 1.5

  if (offset.value >= resetPoint) {
    offset.value = 0
  }

  animationFrame = requestAnimationFrame(moveSlider)
}

const handleNavbarScroll = () => {
  isScrolled.value = window.scrollY > 80
}

const handleScroll = () => {
  const textPosition = window.innerHeight - 100

  const lightSections = document.querySelectorAll('.menu, .location')

  isOnLightSection.value = [...lightSections].some(section => {
    const rect = section.getBoundingClientRect()

    return (
      rect.top <= textPosition &&
      rect.bottom >= textPosition
    )
  })
}

const menuOpen = ref(false)

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}

const closeMenu = () => {
  menuOpen.value = false
}

onMounted(async () => {
  window.addEventListener('scroll', handleNavbarScroll)
  window.addEventListener('scroll', handleScroll)

  handleNavbarScroll()
  handleScroll()

  const imgs = track.value?.querySelectorAll('img') || []

  await Promise.all(
    [...imgs].map(img => {
      if (img.complete) return Promise.resolve()

      return new Promise(resolve => {
        img.onload = resolve
        img.onerror = resolve
      })
    })
  )

  resetPoint = track.value.scrollWidth / 2

  console.log('scrollWidth:', track.value.scrollWidth)
  console.log('resetPoint:', resetPoint)

  moveSlider()
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleNavbarScroll)
  window.removeEventListener('scroll', handleScroll)

  if (animationFrame) {
    cancelAnimationFrame(animationFrame)
  }
})
</script>

<style scoped>

.navbar {
    position: fixed;
    z-index: 1000;

    display: flex;
    justify-content: space-between;
    align-items: center;

    width: 100%;
    padding: 30px;
    box-sizing: border-box;

    height: 120px;
    transition: all 0.3s ease;
}

.navbar.scrolled {
    height: 70px;
    background-color: #2a18bc;
}

.navbuttons {
    display: flex;
    align-items: center;
    gap: 30px;
}

.navbtn {
    text-decoration: none;
    color: #f0ece1;
    font-size: 20px;
    transition: 0.3s ease-in-out;    
}

.navbtn:hover {
    color: rgb(240, 202, 140);
}

.logo {
    height: 90px;
    transition: all 0.3s ease;
    z-index: 999;
}

.navbar.scrolled .logo {
    height: 60px;
    z-index: 999;

}

.ig-icon {
    height: 26px;
    align-content: center;
    position: relative;
    top: 1px;
    transition: 0.3s ease-in-out;
}

.ig-icon:hover{
    scale: 1.15;
}

.header {
    position: relative;
    height: 100vh;
    overflow: hidden;
    background: #2a18bc;
    width: 100%;
}

.header-slider {
    position: absolute;
    inset: 0;
    overflow: hidden;
}

.header-track {
    display: flex;
    width: max-content;
    will-change: transform;
}

.header-slide {
    position: relative;
    height: 100vh;
    flex-shrink: 0;
}

.header-slide img {
    display: block;
    height: 100vh;
    width: auto;
}

.header-slide::after {
    content: "";
    position: absolute;
    inset: 0;
    background: rgba(0,0,0,0.25);
}

.header-nav {
    position: absolute;
    top: 50%;
    left: 0;
    width: 100%;
    padding: 0 40px;
    box-sizing: border-box;

    display: flex;
    justify-content: space-between;

    transform: translateY(-50%);
    z-index: 20;
}

.header-btn {
    width: 60px;
    height: 60px;
    border: none;
    border-radius: 50%;
    font-size: 32px;
    cursor: pointer;

    background: #f0ece1;
    color: #2a18bc;
}

.header-avantitle{
    color: white;
    position: absolute;
    left: 50%;
    top: 24%;
    font-size: 32px;
    letter-spacing: 3px;
    transform: translate(-50%, -50%);
    font-family: 'EditorCondensed-Light';
    font-weight: 100;
    text-align: center;
}

.header h1 {
    position: absolute;
    z-index: 10;

    left: 50%;
    top: 47%;

    transform: translate(-50%, -50%);

    color: #f0ece1;
    font-size: 240px;
    margin: 0;
}

.services {
    display: flex;
    gap: 40px;
    position: absolute;
    z-index: 100;
    top: 67.5%;
    width: 100%;
    justify-content: center;
}

.dog-friendly {

    display: flex;
    align-items: center;
    gap: 8px;
}

.dog-icon {
        height: 36px;
}

.service {
    color: #f0ece1;
    font-size: 24px;
    font-family: 'EditorCondensed-Light';
    font-weight: 100;
    letter-spacing: 1px;
}

.nook-coffee{
    position: fixed;
    color: #f0ece1;
    left: -20px;
    bottom: 80px;
    transform: rotate(-90deg);
    margin: 0px;
    font-size: 16px;
    transition: color 0.3s ease;
}

.nook-coffee.blue {
    color: #2a18bc;
}

.about{
    background-color: #2a18bc;
    margin: 0;
    color: #f0ece1;
    padding: 180px 80px;
    text-align: center;
}

.about h1 {
    margin: 0;
    margin-bottom: 30px;
    font-size: 64px;
}

.about p {
    max-width: 1200px;
    text-align: center;
    margin: 0 auto;
    font-size: 48px
}

.menu {
    padding: 160px 80px 60px;
    color: #2a18bc;
    background-color: #f0ece1;
}

.menu h1{
    color: #2a18bc;
    font-size: 150px;
    text-align: center;
    margin: 0;
}

.menu h2{
    color: #2a18bc;
    font-size: 107px;
    text-align: center;
    margin: 0;
    position: relative;
    bottom: 52px;
    font-family: 'EditorCondensed-Light';
    font-weight: 100;
    margin-bottom: -40px;
}

.menu-list {
    list-style: none;
    padding: 0;
    max-width: 800px;
    margin: 50px auto;
}

.menu-item {
    display: flex;
    justify-content: space-between;
    align-items: end;
    padding: 30px 0 0px 0;
    border-bottom: 1px solid #2a18bc;
    font-size: 24px;
    font-weight: 200;
    gap: 10px;
}

.menu-2{
    background-color: #2a18bc;
    color: #f0ece1;
    padding: 30px 80px 140px;
}

.menu-2 h1{
    font-size: 120px;
    text-align: center;
    margin: 0;
}

.menu-2 h2{
    font-size: 64px;
    text-align: center;
    margin: 0;
}

.menu-item2 {
    display: flex;
    justify-content: space-between;
    align-items: end;
    padding: 30px 0 0px 0;
    border-bottom: 1px solid white;
    font-size: 24px;
    font-weight: 600;
    gap: 60px;
}

.price {
    font-family: 'EditorCondensed-Light';
    font-weight: 100;
    font-size: 32px;
}

.sub-item {
    margin: 0;
    font-size: 23px;
    font-weight: 100;
    padding-bottom: 3px;
}

.location {
    background: #f0ece1;
    color: #2a18bc;
    padding: 200px 80px;
}

.location-content {
    max-width: 1500px;
    margin: 0 auto;

    display: grid;
    grid-template-columns: 1fr 1.2fr;
    gap: 80px;
    align-items: center;
}

.location-tag {
    font-size: 14px;
    letter-spacing: 4px;
    margin-bottom: 30px;
    margin-top: 0;
}

.location h1 {
    font-size: 120px;
    line-height: .9;
    margin-bottom: 50px;
    margin-top: 44px;
}

.location-address {
    font-size: 40px;
    margin-bottom: 45px;
    font-family: 'EditorCondensed-Light';
    font-weight: 100;
}

.location-hours {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-bottom: 45px;
}

.hours-row {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid #2a18bc;
    padding-bottom: 2px;
    font-size: 20px;
}

.directions-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;

    padding: 18px 36px;

    background: #2a18bc;
    color: #f0ece1;

    text-decoration: none;
    font-weight: 600;
    letter-spacing: 1px;

    transition: .3s ease;
    letter-spacing: 2px;
}

.directions-btn:hover {
    transform: translateY(-4px);
}

.location-map {
    width: 100%;
}

.mapa {
    width: 100%;
    height: 650px;
    border: none;
    border: 0px solid #2a18bc;
}

.contact {
    background: #2a18bc;
    color: #f0ece1;

    padding: 180px 80px;

    display: flex;
    flex-direction: column;
    align-items: center;
}

.contact-tag {
    font-size: 14px;
    letter-spacing: 4px;
}

.contact h1{
    font-size: 120px;
    margin-bottom: 50px;
    margin-top: 30px;
    text-align: center;
}

.contact-description {
    font-size: 40px;
    text-align: center;
    max-width: 700px;
    margin-top: 0;
    margin-bottom: 80px;
    font-family: 'EditorCondensed-Light';
    font-weight: 100;
}

.contact-form {
    width: 100%;
    max-width: 700px;

    display: flex;
    flex-direction: column;
    gap: 30px;
}

.contact-form input,
.contact-form textarea {
    background: transparent;
    border: none;
    border-bottom: 1px solid rgba(240,236,225,.5);

    padding: 20px 0;

    color: #f0ece1;
    font-size: 22px;

    outline: none;
    font-family: Helvetica;
    width: 100%;
}

.contact-form input::placeholder,
.contact-form textarea::placeholder {
    color: rgba(240,236,225,.45);
}

.contact-form button {
    margin-top: 20px;

    background: #f0ece1;
    color: #2a18bc;

    border: none;

    padding: 20px;

    font-size: 18px;
    font-weight: 700;

    cursor: pointer;

    transition: .3s ease;
    letter-spacing: 2px;
}

.contact-form button:hover {
    transform: translateY(-4px);
}

.footer{
    background-color: #2a18bc;
    color: #f0ece1;
    display: flex;
    gap: 30px;
    justify-content: center;
    padding: 30px 80px;
}

.footer a{
    color:#f0ece1;
    text-decoration: none;    
}

.hamburger {
    display: none;
    flex-direction: column;
    justify-content: center;
    gap: 6px;

    width: 42px;
    height: 42px;

    background: transparent;
    border: none;
    cursor: pointer;
    z-index: 2000;
}

.hamburger span {
    width: 100%;
    height: 3px;
    background: #f0ece1;
    transition: .3s;
}

.hamburger.active span:nth-child(1) {
    transform: translateY(9px) rotate(45deg);
}

.hamburger.active span:nth-child(2) {
    opacity: 0;
}

.hamburger.active span:nth-child(3) {
    transform: translateY(-9px) rotate(-45deg);
}

@media (max-width: 1400px) {
    .header h1 {
        font-size: 200px;
    }
}

@media (max-width: 1200px) {
    .header h1 {
        font-size: 175px;
    }
}

@media (max-width: 1000px) {
    .header h1 {
        font-size: 130px;
    }
    .header-avantitle{
        font-size: 24px;
        top: 30%;
    }
    .services {
        scale: 90%;
        flex-wrap: wrap;
        top: 62%;
    }
    .menu h1{
    font-size: 120px;
    text-align: center;
    margin: 0;
}

.menu h2{
    font-size: 86px;
    text-align: center;
    margin: 0;
    margin-top: 10px;
}

.location-content {
    grid-template-columns: 1fr;
}
}

@media (max-width: 769px) {
    .header h1 {
        font-size: 110px;
    }
    .header-avantitle{
        font-size: 20px;
    }

    .about p{
        font-size: 32px;
    }
    .services {
        scale: 80%;
        top: 60%;
    }
        .hamburger{
        display:flex;
    }

    .navbuttons{
        position: fixed;

        top: 0;
        right: -100%;

        width: 280px;
        height: 100vh;

        background: #2a18bc;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        gap: 40px;

        transition: .35s ease;
    }

    .navbuttons.open{
        right:0;
    }

    .navbtn{
        font-size:30px;
    }

    .ig-icon{
        height:34px;
    }

    .header h1 {
        font-size: 110px;
    }

    .header-avantitle{
        font-size:20px;
    }

    .services{
        scale:80%;
        top:60%;
    }
        .menu h1{
    font-size: 90px;
    text-align: center;
    margin: 0;
}

.menu h2{
    font-size: 64px;
    text-align: center;
    margin: 0;
    margin-top: 25px;
}

.location h1 {
    font-size: 90px;
}

.contact h1 {
    font-size: 90px;
}
}

@media (max-width: 650px) {
    .header h1 {
        font-size: 90px;
    }
    .header-avantitle{
        font-size: 16px;
    }
    .services {
        scale: 70%;
        top: 58%;
    }
    .mapa {
    width: 100%;
    height: 450px;
    border: none;
    border: 0px solid #2a18bc;
}
}

@media (max-width: 550px) {
    .header h1 {
        font-size: 75px;
    }
.footer {
    font-size: 12px;
}
}

@media (max-width: 480px) {
    .header h1 {
        font-size: 65px;
    }
        .services {
    top: 56%;
    }
            .menu h1{
    font-size: 65px;
    text-align: center;
    margin: 0;}

        .about p{
        font-size: 28px;
    }

    .hours-row {
        font-size: 16px;
    }

.menu h2{
    font-size: 48px;
    text-align: center;
    margin: 0;
    margin-top: 30px;
}

.menu-item {
    font-size: 20px;
    gap: 10px;

}

.menu-item2 {
    font-size: 20px;
    gap: 10px;
}

.sub-item {
    font-size: 19px;
}

.price {
    font-size: 24px;
}

.mapa {
    width: 100%;
    height: 350px;
    border: none;
    border: 0px solid #2a18bc;
}

.footer {
    font-size: 10px;
}
}

@media (max-width: 400px) {
    .header h1, .menu h1, .about h1, .location h1, .contact h1 {
        font-size: 58px;
    }
    
    .menu h2 {
        font-size: 42px;
        margin-top: 35px;
    }

    .menu-item {
        display: flex;
        flex-wrap: wrap;
        width: 100%;
    }

    .menu-item span {
        width: 100%;
    }

        .menu-item2 {
        display: flex;
        flex-wrap: wrap;
        width: 100%;
    }
        .menu-item2 span {
        width: 100%;
    }
}

@media (max-width: 360px) {
    .header h1 {
        font-size: 50px;
    }
    .services {
        scale: 65%;
        top: 56%;
    }
}

</style>
