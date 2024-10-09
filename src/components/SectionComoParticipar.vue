<script setup>
 const images = ["https://placehold.jp/f7efd8/ffffff/360x360.png", "https://placehold.jp/f7efd8/ffffff/360x360.png", "https://placehold.jp/f7efd8/ffffff/360x360.png", "https://placehold.jp/f7efd8/ffffff/360x360.png"]
</script>


<template>
    <section class="section__como__participar">
        <div class="container__como__participar">
            <h2 class="section__como__participar__titulo">COMO PARTICIPAR</h2>
            <div class="section__como__participar__imagem">
                <div v-for="image in images" :key = "image">
                    <img id="section__como__participar__imagem" :src="image" alt="">
                </div>
            </div>  
            <div class="section__como__participar__button">
                <button type="button" id="button__como__participar">
                    CADASTRAR-SE
                </button>
            </div>
        </div>
    </section>
</template>

<style scoped>

    .section__como__participar{
        display: grid;
        grid-template-columns: repeat(8,1fr);
    }

    .container__como__participar{
        grid-column: 1 / span 8;
        display: grid;
        grid-template-columns: repeat(8,1fr);
        justify-content: center;
        align-items: center;
        margin-top: 50px;
        gap: 50px;
    }

    .section__como__participar__titulo{
        grid-column: 1 / span 8;
        width: 100%;
        text-align: center;
        margin-top: 2rem;
        margin-bottom: 4rem;
        color: #666666;
        font-size: 2rem;
        
    }
    .section__como__participar__imagem{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 53px;
        margin-bottom: 3rem;
        grid-column: 1 / span 8;
    }

    #section__como__participar__imagem{
        width: 100%;
    }

    .section__como__participar__button{
        grid-column: 3 / span 4;
        display: flex;
        justify-content: center;
        margin-bottom: 4rem;
    }

    #button__como__participar{
        width: 100%;
        border-radius: 48px;
        color: #fff;
        background-color: #273142;
        text-decoration: none;
    }

@media (max-width: 400px){
    #section__como__participar__imagem{
        width: 100%;
        max-width: 280px;
    }

    .section__como__participar__button{
        grid-column: 2 / span 6;
       
    }
}

@media (max-width: 380px){
    #section__como__participar__imagem{
        width: 100%;
        max-width: 200px;
    }

    .section__como__participar__titulo{
        font-size: 1.8rem;
    }

}

@media (max-width: 320px){
    #section__como__participar__imagem{
        width: 100%;
        max-width: 200px;
    }

    
}
   
    
</style>

