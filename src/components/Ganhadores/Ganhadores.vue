<script setup>
    import Accordion from "./Accordion.vue";
    import { onMounted, ref } from "vue";

onMounted(() => {
    
    fetchGanhadores()
  
});

const ganhadores = ref([])

const fetchGanhadores = async () => {
    try {
        const response = await fetch('https://apiwinners.onrender.com/winners');
        const data = await response.json();

        const groupedGanhadores = {}; 

        data.forEach(ganhador => {
            const date = ganhador.date; 
            if (!groupedGanhadores[date]) { 
                groupedGanhadores[date] = []; 
            }
            groupedGanhadores[date].push(ganhador);
        });

        ganhadores.value = Object.entries(groupedGanhadores).map(([date, winners]) => ({ //
            date,
            winners
        }));

    } catch (error) {
        console.error('erro ao buscar ganhadores:', error);
    }
}


</script>
    
<template>
    <div class="componente-ganhadores">
        <Accordion v-for="(ganhador,index) in ganhadores" :key="ganhador.date" :ganhadores="ganhador.winners" :index="index" />
    </div>
</template>

<style scoped>
    .componente-ganhadores{
        width: 100%;
        background: transparent;
        margin-inline: auto;
        padding: 2rem;
        display: flex;
        flex-direction: column;
        gap: 3rem 0;
    }
</style>

