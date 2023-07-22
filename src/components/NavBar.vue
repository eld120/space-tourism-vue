<script setup lang="ts">


</script>
<template>
    <nav class="navbar">
        <ul>
            <li><a href=""><span>00</span>Home</a></li>
            <li><a href=""><span>01</span>Destination</a></li>
            <li><a href=""><span>02</span>Crew</a></li>
            <li><a href=""><span>03</span>Technology</a></li>
        </ul>
        <button  id="hamburger"></button>
    </nav>
</template>
<style scoped lang="sass">
nav 
    min-height: 4em
    width: 100vw
    display: flex
    
    
    ul 
        display: flex
        flex-direction: column
        padding: 0
        
        
        
    
    li 
        
        list-style-type: none
        margin: auto auto auto 0
        a 
            span 
                margin: 0 1em
            
            color: white
        
    
    button
        border: none
        background: url('../assets/icon-hamburger.svg')
        border-radius: 0px
        height: 1.3em
        width: 1.7em
        padding: 0
        margin: auto 2em auto auto
    
    

@media only screen and (min-width: 768px)
        nav 
            ul
            flex-direction: row
            
        
    
    @media only screen and (min-width: 992px) 
        #hamburger
            display: none
        
        
    
</style>
