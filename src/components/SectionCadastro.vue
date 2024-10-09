<template>
    <section class="section__cadastro">
        <div class="section__cadastro__imagem">
            <img id="section__cadastro__imagem" src="https://placehold.jp/f7efd8/ffffff/700x400.png" alt="">
        </div>
        <div class="section__cadastro__button">
            <button type="button" id="button__cadastro">
                CADASTRAR-SE
            </button>
        </div>
    </section>
</template>

<style scoped>
    .section__cadastro{
        display: grid;
        grid-template-columns: repeat(8,1fr);
        grid-template-rows: auto;
        row-gap: 6rem;
        width: 100%;
        max-width: 1520px;
        margin-top: 50px;
    }

    .section__cadastro__imagem{
        display: flex;
        justify-content: center;
        margin-top: 150px;
        grid-column: 3 / span 4;
    }

    #section__cadastro__imagem{
        width: 100%;
        height: 500px;
        margin-top: 5rem;
        margin-bottom: 3rem;
    }

    .section__cadastro__button{
        grid-column: 3 / span 4;
        margin-bottom: 4rem;
    }

    #button__cadastro{
        width: 100%;
        border-radius: 48px;
        background-color: #273142;
        color: #fff;
        text-decoration: none;
    }

    @media (max-width: 1024px){

    .section__cadastro__imagem{
        grid-column: 2 / span 6;
    }

    #section__cadastro__imagem{
        width: 100%px;
        height: 350px;
        margin-top: 200px;

    }

    .section__cadastro__button{
        grid-column: 2 / span 6;
        margin-bottom: 15rem;
    }
        
    }

    @media (max-width: 400px){

    }


    
</style>