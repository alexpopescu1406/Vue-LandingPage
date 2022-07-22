<template>
  <div
    data-aos="fade-down-right"
    data-aos-delay="50"
    data-aos-duration="1000"
    data-aos-easing="ease-in-out-quad"
    data-aos-mirror="false"
    data-aos-once="true"
    anchorPlacement="bottom">
<div class="about" id="c1">
    <h1>{{ about }}</h1> 
        <div class="abouttextcss">
            {{ msg1 }}<br>
            {{ msg2 }}<br> 
            {{ msg3 }}<br>
        </div>  
    <h1>{{ follow }}</h1>
    <div class="media">
        <a href="https://facebook.com" target="_blank">
            <img :src="facebook" alt="facebook">
        </a>
        <a href="https://youtube.com" target="_blank">
            <img :src="youtube" alt="youtube"> 
        </a>
        <a href="https://instagram.com" target="_blank">
            <img :src="instagram" alt="instagram">
        </a>
</div>
</div>
</div>

</template>

<script>
export default {
    name: 'About',

data () {
  return {
    about: 'ABOUT US',
    follow: 'FOLLOW US',
    msg1: 'Providing legendary mobile games.',
    msg2: 'Dedicated team of mobile games developers.',
    msg3: 'We are based in Bucharest.',
    facebook: 'https://imagizer.imageshack.com/v2/xq90/922/YQYc7D.png',
    youtube: 'https://imagizer.imageshack.com/v2/xq90/923/0qIVCk.png',
    instagram: 'https://imagizer.imageshack.com/v2/xq90/922/W4Lkoe.png'
}}
}

</script>

<style scoped>
.media {
    text-align: center;
}
.abouttextcss {
    color: white;
    text-align: center;
    font-size: 20px;
}
</style>