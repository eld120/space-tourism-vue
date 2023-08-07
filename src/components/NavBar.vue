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
<style scoped lang="sass">
nav 
    min-height: 4em
    width: 100vw
    display: flex
    padding: 0 1.5em 
    
    img
        max-width: 2.5em
        max-height: 2.5em
        margin: auto auto auto 0
    
        
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
        margin: auto 0 auto auto
        // display: block
        // position: relative
        z-index: 1
        -webkit-user-select: none
        -moz-user-select: none
        -ms-user-select: none
        user-select: none
    .menu
        display: flex
        flex-direction: column
        position: absolute
        background: rgb(150, 150, 150, 0.7)
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


@media only screen and (min-width: 766px)
    nav 
        padding: 0 0 0 1.5em
        margin-bottom: 6.8125em
        li
            margin: auto 1.25em
        button
            display: none
        .menu
            flex-direction: row
            position: static
            margin: 0
            padding: 0
            height: 6em  
            width: 28.125em
            margin: 0
            padding: 0
            background: rgb(150, 150, 150, 0.1)
            justify-content: center
            
            /* Hide the menu off-screen to the left */
            right: 0
        .bold
            display: none
    
@media only screen and (min-width: 992px) 
    #hamburger
        display: none
    
    
    
</style>
