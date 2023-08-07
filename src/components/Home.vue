<script setup lang="ts">
import { ref } from 'vue'

// defineProps<{  }>()
const headerIntro = ref("So, you want to travel to")

</script>

<template>
 <p class="nav-text">{{ headerIntro.toUpperCase() }}</p> 
 <h3 class="heading-two-mobile">SPACE</h3>
    
 
    <div class="section">
        <p class="p-mobile">
            Let’s face it; if you want to go to space, you might as well genuinely go to
            outer space and not hover kind of on the edge of it. Well sit back, and relax
            because we’ll give you a truly out of this world experience!
        </p>
        <div class="circle"><span class="explore">Explore</span></div>
    </div>

</template>
 

<style scoped lang="sass">
.section
    display: flex
    flex-direction: column
    height: 100%

    
    
    
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
@media only screen and (min-width: 768px)
    .section
        max-width: 28.125em
    .circle
        height: 15.125em
        width: 15.125em
        border-radius: 10em
        bottom:5.625em
    .explore
        font-size: 2em
</style>
