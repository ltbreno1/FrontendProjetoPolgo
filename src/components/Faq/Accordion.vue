<script setup>
import { ref } from "vue";
import SlideUpDown from "vue-slide-up-down";

const props = defineProps({
    duvida: {
        type: Object,
        required: true, 
    },
});

const visible = ref(false); 

function handleToggleAccordionVisible() {
    visible.value = !visible.value;
}
</script>

<template>
    <section class="section__accordion">
        <div class="componente-accordion">
            <div @click="handleToggleAccordionVisible" class="accordion__header">  
                <span class="accordion__title">{{ duvida.label }}</span>  
                <div class="accordion__icon">
                    <div class="accordion__line"></div>
                    <div class="accordion__line accordion__line-vertical" :class="{ 'accordion__line-vertical-active': visible}"></div>  
                </div>
            </div>
            <SlideUpDown :active="visible" class="woobly-accordion" :duration="400">  
                <div class="accordion__content" v-html="duvida.conteudo"></div>
            </SlideUpDown>
        </div>
    </section>
</template>

<style scoped>

    .section__accordion{
        display: flex;
        justify-content: center;
        
    }

    
    .componente-accordion {
        background-color: #556270;
        border-radius: 25px;
        padding-inline: 25px;
        width: 1520px;
    }

    .componente-accordion:last-child{
        border-bottom:none;
    }

    .accordion__header{
        cursor:pointer;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-block: 1.5rem;
    }

    .accordion__title{
        font-size: 1.25rem;
        font-weight: 700;
        pointer-events: none;
        color: #fff;
    }  

    .accordion__icon{
        width: 1.5rem;
        height: 1.5rem;
        border: 2px solid #fff;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        position: relative;
        align-items: center;
        pointer-events: none; 
    }

    .accordion__line{
        width: 0.75rem;
        height: 2px;
        border-radius: 1px;
        background: #fff;
    }

    .accordion__line-vertical{
        position: absolute;
        transform: rotate(90deg);
        transition: transform 0.4; 
    }

    .accordion__line-vertical-active{
        transform: rotate(180deg);
    }

    .woobly-accordion{
        transition-timing-function: ease-in-out;
    }

    .accordion__content{
        padding-bottom: 1.5rem;
        color: #fff;
    }
</style>