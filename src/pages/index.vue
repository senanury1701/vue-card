<script setup>
import vueLogo from '../assets/vue.svg'
import languages from '../helper/data'
import Card from '../components/card.vue'

</script>
<template>
    <div >
        <a href="#" target="_blank">
            <img :src="vueLogo" className="logo react" alt="React logo" />
        </a>
    </div>
    <div className='card-container' >
        <div className='grid-container'>
            <div v-for="data in languages" :key="data">
                <Card :data="data"/>                  
            </div>
   
        </div>
    </div>
</template>
<style>
.logo {
    height: 6.5em;
    margin: 2rem;
    will-change: filter;
    transition: filter 300ms;
  }

  .logo:hover {
    filter: drop-shadow(0 0 2em #ffffff);
    transform: scale(1.3);
  }
  .logo.react:hover {
    filter: drop-shadow(0 0 2em #10bb4f);
  }
  
  
  @media (prefers-reduced-motion: no-preference) {
    a:nth-of-type(2) .logo {
      animation: logo-spin infinite 20s linear;
    }
  }
  
  .card-container{
    width: 500px;
    margin-top: 1rem;
    border-radius: 15px;
    background: rgb(105, 200, 155);
    background: -moz-radial-gradient(top left, ellipse cover, rgba(144, 238, 144, 1) 0%, rgba(34, 139, 34, 1) 100%);
    background: -webkit-gradient(radial, top left, 0px, top left, 100%, color-stop(0%, rgba(144, 238, 144, 1)), color-stop(100%, rgba(34, 139, 34, 1)));
    background: -webkit-radial-gradient(top left, ellipse cover, rgba(144, 238, 144, 1) 0%, rgba(34, 139, 34, 1) 100%);
    background: -o-radial-gradient(top left, ellipse cover, rgba(144, 238, 144, 1) 0%, rgba(34, 139, 34, 1) 100%);
    background: -ms-radial-gradient(top left, ellipse cover, rgba(144, 238, 144, 1) 0%, rgba(34, 139, 34, 1) 100%);
    background: radial-gradient(ellipse at top left, rgba(144, 238, 144, 1) 0%, rgb(22, 81, 22) 100%);
    filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#90ee90', endColorstr='#228b22', GradientType=1);
    box-shadow: rgba(0, 0, 0, 0.631) 10px 10px;
  }

  .grid-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(4, 1fr);
    grid-column-gap: 10px;
    grid-row-gap: 10px;
    padding: 20px;
  
  }


  
</style>