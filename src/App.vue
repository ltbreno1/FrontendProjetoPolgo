<script setup>
import Header from './components/Header.vue'
import SectionCadastro from './components/SectionCadastro.vue'
import SectionComoParticipar from './components/SectionComoParticipar.vue'
import SectionCarrossel from './components/SectionCarrossel.vue'
import SectionDuvidas from './components/SectionDuvidas.vue'
import SectionGanhadores from './components/SectionGanhadores.vue'
import Faq from './components/Faq/Faq.vue'
import Ganhadores from './components/Ganhadores/Ganhadores.vue'
import Footer from './components/Footer.vue'

</script>

<template>
  <div class="app"> 
    <Header />
    <SectionCadastro />
    <SectionComoParticipar />
    <div><SectionCarrossel /></div>
    <SectionDuvidas />
    <Faq />
    <SectionGanhadores />
    <Ganhadores />
    <Footer />
  
    
  </div>

  
</template>

<style scoped>
.app{
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  background-color: #fff;
  width: 100%;
}

</style>
