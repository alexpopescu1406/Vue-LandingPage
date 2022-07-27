<template>
    <div
    data-aos="zoom-out-up"
    data-aos-delay="100"
    data-aos-duration="1000"
    data-aos-easing="ease-in-out"
    data-aos-mirror="false"
    data-aos-once="true"
    data-aos-offset="600">

    <div class="play">
    <h2 class="playtext">{{ play }}</h2>
        <a href="https://play.google.com/store/apps/details?id=com.TopLexGames.CaptainSmashTok&gl=RO" target="_blank">
            <img class="android" :src="require('../../images/google-play-badge.png')" alt="google">
        </a>
        <a href="https://www.apple.com/app-store/" target="_blank"> 
            <img class="apple" :src="require('../../images/apple.png')" alt="ios">
        </a>
        <div id="c5"></div>
    </div>
    </div>
</template>

<script>
export default {
    name: 'Platforms',
data () {
    return {
        play: 'PLAY ON:'
        }
    }
};
</script>

<style scoped>
.play {
    padding: 10px;
    height: 200px;
}

.playtext {
    color: white;
    font-weight: bold;
    font-size: 30px;
    text-align: center;
}

.android {
    margin-left: 500px;
    width: 350px;
    height: 150px;
}

.apple {
    margin-left: 200px;
    width: 300px;
    height: 100px;
}
</style>