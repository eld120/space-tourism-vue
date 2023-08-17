<script setup lang="ts">
import { ref } from 'vue'

// defineProps<{  }>()
const headerIntro = ref("So, you want to travel to")

</script>

<template>
 <section class="main">
     <p class="nav-text">{{ headerIntro.toUpperCase() }}</p>
     <h3 class="heading-two">SPACE</h3>
     
     
        <div class="main-text">
            <p class="p-mobile">
                Let’s face it; if you want to go to space, you might as well genuinely go to
                outer space and not hover kind of on the edge of it. Well sit back, and relax
                because we’ll give you a truly out of this world experience!
            </p>
            <div class="circle"><span class="explore">Explore</span></div>
        </div>
 </section>

</template>
 

<style scoped lang="sass">
.main
    place-items: center
    text-align: center
    display: flex
    flex-direction: column
.main-text
    display: flex
    flex-direction: column
    height: 100%
    max-width: 70%
.heading-two
    font-size: 5em
    
    
    
.p-mobile
    font-size: 0.9375em
    font-family: 'Barlow', sans-serif 
    line-height: 1.5625em
    margin-bottom: 3em
.explore
    color: black
    font-size: 1.25em
    font-family: 'Bellefair', serif
    margin: auto
    position: relative
    bottom: -39%
.circle
    position: absolute
    bottom: 3em
    right: 50%
    left: 50%
    transform: translate(-50%, 0%)
    background: white
    border-radius: 5em
    height: 9.375em
    width: 9.375em
    margin: auto auto 0 auto
    z-index: 1
@media only screen and (min-width: 766px)
    .main-text
        max-width: 28.125em
        z-index: 1
    .circle
        height: 15.125em
        width: 15.125em
        border-radius: 10em
        bottom:5.625em
    .explore
        font-size: 2em

@media only screen and (min-width: 990px)  
.main
    text-align: left
    justify-content: start
    height: 100%
    align-items: start
    padding-left: 5em
    .nav-text
        font-size: 1.75em
    .heading-two
        font-size: 9.375em 
    .p-mobile
        font-size: 1.125em
        
    .circle
        // height: 17.125em
        // width: 17.125em
        border-radius: 12em
        text-align: center
        bottom: 1%
        right: 25%
        left: 80%
</style>
