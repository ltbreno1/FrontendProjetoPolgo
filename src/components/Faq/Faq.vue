<script setup>
    import Accordion from "./Accordion.vue";

    const duvidas = [
        {
            label: "Duvida 1",
            conteudo: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
        },
        {
            label: "Duvida 2",
            conteudo: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
        },
        {
            label: "Duvida 3",
            conteudo: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
        },
        {
            label: "Duvida 4",
            conteudo: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
        },
        {
            label: "Duvida 5",
            conteudo: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
        },
        {
            label: "Duvida 6",
            conteudo: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
        },
    ];
</script>

<template>
    <div class="componente-faq">
        <Accordion v-for="duvida in duvidas" :key="duvida.label" :duvida="duvida" />
    </div>
</template>

<style scoped>
    .componente-faq{
        width: 100%;
        background: transparent;
        margin-inline: auto;
        padding: 2rem;
        display: flex;
        flex-direction: column;
        gap: 3rem 0;
    }
</style>