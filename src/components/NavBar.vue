<script setup lang="ts">
    import { ref } from 'vue';
    let hamburgerToggle = ref(false)
    
    function menuToggle(){
        hamburgerToggle.value = !hamburgerToggle.value
        
    }
</script>
<template>
    <nav class="navbar" role="navigation" aria-expanded="false">
        <img src="../assets/logo.svg" alt="SPACE WEBSITE LOGO">
        <ul class="menu" :class="{'expand': hamburgerToggle}">
            <li><a href="" class="nav-text"><span class="bold">00</span>Home</a></li>
            <li><a href="" class="nav-text"><span class="bold">01</span>Destination</a></li>
            <li><a href="" class="nav-text"><span class="bold">02</span>Crew</a></li>
            <li><a href="" class="nav-text"><span class="bold">03</span>Technology</a></li>
        </ul>
        <button  id="hamburger" @click="menuToggle" :class="{'hamburger-toggle': hamburgerToggle}"><span class="hidden-but-accessible">Menu</span></button>
        
    </nav>
</template>
<style  lang="sass">
nav 
    min-height: 4em
    width: 100vw
    display: flex
    
    img
        max-width: 2.5em
        max-height: 2.5em
        margin: auto auto auto 1.5em
    ul 
        display: flex
        flex-direction: column
        padding: 0
    li 
        list-style-type: none
        margin: .5em auto .5em 0
    a 
        span 
            margin: 0 1em
      
        color: white
        -webkit-transition: color 0.3s ease
        -o-transition: color 0.3s ease
        transition: color 0.3s ease
    a:hover
        color: #D0D6F9
    button
        border: none
        background: url('../assets/icon-hamburger.svg')
        border-radius: 0px
        height: 1.3125em
        width: 1.5em
        padding: 0
        margin: auto 1.5em auto auto
        display: block
        position: relative
        z-index: 1
        -webkit-user-select: none
        -moz-user-select: none
        -ms-user-select: none
        user-select: none
    .menu
        position: absolute
        background: #0B0D17
        width: 300px
        margin: -100px 0 0 -50px
        padding: 50px
        padding-top: 125px
        height: 100vh
        list-style-type: none
        /* Hide the menu off-screen to the left */
        right: -100%
        -webkit-transition: right 0.3s ease
        -o-transition: right 0.3s ease
        transition: right 0.3s ease
    .expand
        right: 0
    .hamburger-toggle
        background: url('../assets/icon-close.svg')
        background-repeat: no-repeat


@media only screen and (min-width: 768px)
        nav 
            ul
                flex-direction: row
            li
                margin: auto auto auto 0
            button:
                display: none
    
@media only screen and (min-width: 992px) 
    #hamburger
        display: none
    
        
    
</style>
