<template>
<Header />

  <div id="c1"></div>
  <img src="../images/horizline.png" alt="line" class="horizline">

<About /><br>
<div v-if="showModal1">
<LogIn @close="toggleModal1"> </LogIn>
</div>
<div
    data-aos="fade-down-right"
    data-aos-delay="0"
    data-aos-duration="1000"
    data-aos-easing="ease-in-out-quad"
    data-aos-mirror="false"
    data-aos-once="true"
    data-aos-offset="-20"
    anchorPlacement="bottom">
<button class="button-65" @click="toggleModal1">Register</button>
</div><br>

<div v-if="showModal">
<Register @close="toggleModal">
  <h2><b>Subscribe to our Newsletter</b></h2>
  <p><b>Get the latest news and best offers!</b></p>
  
</Register>
</div>
<div
    data-aos="fade-down-right"
    data-aos-delay="0"
    data-aos-duration="1000"
    data-aos-easing="ease-in-out-quad"
    data-aos-mirror="false"
    data-aos-once="true"
    data-aos-offset="-20"
    anchorPlacement="bottom">
<button class="button-65" @click="toggleModal">Subscribe</button>
</div>

  <div id="c2"></div>
  <img src="../images/horizline.png" alt="line" class="horizline">

<Games />

  <div id="c3"></div>
 <img src="../images/horizline.png" alt="line" class="horizline">

<Platforms />

 <img src="../images/horizline.png" alt="line" class="horizline">

<ComingSoon />
<Countdown />

 <img src="../images/horizline.png" alt="line" class="horizline">

<Contact />
</template>

<script>
import Contact from './components/Contact.vue'
import ComingSoon from './components/ComingSoon.vue'
import Header from './components/Header.vue'
import About from './components/About.vue'
import Games from './components/Games.vue'
import Platforms from './components/Platforms.vue'
import Countdown from './components/Countdown.vue'
import Register from './components/Register.vue'
import LogIn from './components/LogIn.vue'

export default {
  name: 'App',
  components: {
    Header,
    About,
    Games,
    Platforms,
    ComingSoon,
    Contact,
    Countdown,
    Register,
    LogIn
},
data () {
  return {
    showModal:  false,
    showModal1: false
  }
},
methods: {
    toggleModal() {
        this.showModal = !this.showModal
    },
    toggleModal1() {
        this.showModal1 = !this.showModal1
    }
}
}
</script> 

<style scoped>  
.horizline {
    display: block;
    max-width: 100%;
    margin-left: auto;
    margin-right: auto;
    padding: 30px;
}
.test {
  color:white;
  font-size: 30px;
  text-align: center;;
}
.button-65 {
  appearance: none;
  backface-visibility: hidden;
  background-color: #2f80ed;
  border-radius: 10px;
  border-style: none;
  box-shadow: none;
  box-sizing: border-box;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-family: Inter,-apple-system,system-ui,"Segoe UI",Helvetica,Arial,sans-serif;
  font-size: 15px;
  font-weight: 500;
  height: 50px;
  letter-spacing: normal;
  line-height: 1.5;
  outline: none;
  overflow: hidden;
  padding: 14px 30px;
  position: relative;
  text-align: center;
  text-decoration: none;
  transform: translate3d(0, 0, 0);
  transition: all .3s;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: nowrap;
  display: block;
  margin: auto;
  
}
.button-65:hover {
  background-color: #1366d6;
  box-shadow: rgba(0, 0, 0, .05) 0 5px 30px, rgba(0, 0, 0, .05) 0 1px 4px;
  opacity: 1;
  transform: translateY(0);
  transition-duration: .35s;
}
.button-65:hover:after {
  opacity: .5;
}
.button-65:active {
  box-shadow: rgba(0, 0, 0, .1) 0 3px 6px 0, rgba(0, 0, 0, .1) 0 0 10px 0, rgba(0, 0, 0, .1) 0 1px 4px -1px;
  transform: translateY(2px);
  transition-duration: .35s;
}
.button-65:active:after {
  opacity: 1;
}
@media (min-width: 768px) {
  .button-65 {
    padding: 14px 22px;
    width: 176px;
  }
}
</style>