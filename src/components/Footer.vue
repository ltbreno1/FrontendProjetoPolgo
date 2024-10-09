<script>
    function updateFooterLayout() {
        const footerPowered = document.getElementById('poweredBy');
        const footerConteudo = document.querySelector('.footer__conteudo');

        if (window.innerWidth <= 780) {
            
            footerConteudo.appendChild(footerPowered);
        } else {
            const footerImages = document.querySelector('.footer__imagens');
            footerImages.appendChild(footerPowered);
        }
    }

    
    window.addEventListener('resize', updateFooterLayout);

    window.addEventListener('DOMContentLoaded', updateFooterLayout);
</script>



<template>
    <footer class="footer">
        <div class="footer__conteudo">
            <div class="footer__imagens">
                <img id="logo__principal" src="https://fakeimg.pl/200x100/" alt="Logo Principal">
                <div id="poweredBy" class="footer__powered">
                    <p>Powered by:</p>
                    <img id="logo__polgo" src="../assets/logo polgo teste.png" alt="Logo Polgo">
                </div>
            </div>

            <div class="footer__conteudo__direita">
                <ul class="footer__conteudo__ul">
                    <li class="footer__conteudo__li">
                        <a class="footer_conteudo__li__a" href="#">Política de privacidade</a>
                    </li>
                    <li class="footer__conteudo__li">
                        <a class="footer_conteudo__li__a" href="#">Termos de uso</a>
                    </li>
                    <li class="footer__conteudo__li">
                        <a class="footer_conteudo__li__a" href="#">Regulamento</a>
                    </li>
                    <li class="footer__conteudo__li">
                        <a class="footer_conteudo__li__a" href="#">SRE: 000000000000000</a>
                    </li>
                </ul>
            </div>

            <div class="footer__conteudo__social">
                <ul class="footer__conteudo__ul__header">
                    <li class="footer__conteudo__li__header">
                        <a href="#"><img class="footer__conteudo__imagem__header" src="../assets/facebook.png" alt="Facebook"></a>
                        <a href="#"><img class="footer__conteudo__imagem__header" src="../assets/instagram.png" alt="Instagram"></a>
                        <a href="#"><img class="footer__conteudo__imagem__header" src="../assets/youtube.png" alt="YouTube"></a>
                        <a href="#"><img class="footer__conteudo__imagem__header" src="../assets/linkedin.png" alt="LinkedIn"></a>
                    </li>
                    <li class="footer__conteudo__li__header">
                        <a class="footer__conteudo__li__a__header" href="#">HOME</a>
                    </li>
                    <li class="footer__conteudo__li__header">
                        <a class="footer__conteudo__li__a__header" href="#">COMO PARTICIPAR</a>
                    </li>
                    <li class="footer__conteudo__li__header">
                        <a class="footer__conteudo__li__a__header" href="#">PRÊMIOS</a>
                    </li>
                    <li class="footer__conteudo__li__header">
                        <a class="footer__conteudo__li__a__header" href="#">DÚVIDAS FREQUENTES</a>
                    </li>
                    <li class="footer__conteudo__li__header">
                        <a class="footer__conteudo__li__a__header" href="#">GANHADORES</a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<style scoped>
.footer {
    position: static;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: #273142;
    display: flex;
    justify-content: center;
    align-items: center;
    padding-inline: 4rem;
    padding-block: 2rem;
}

.footer__conteudo {
    width: 100%;
    max-width: 1520px;
    margin: 0;
    display: grid;
    grid-template-columns: auto 1fr auto; 
    text-align: center; 
}

.footer__imagens {
    display: flex;
    flex-direction: column;
    align-items: flex-start; 
    gap: 100px;
}

.footer__conteudo__direita {
    display: flex;
    flex-direction: column;
    align-items: center; 
    gap: 1rem; 
}

.footer__conteudo__ul {
    width: 100%;
    padding: 0; 
    margin: 0; 
    list-style-type: none;
    display: flex; 
    flex-direction: column; 
    gap: 3rem; 
}

.footer__conteudo__ul__header{
    width: 100%;
    padding: 0;
    margin: 0;
    list-style-type: none;
    display: flex;
    flex-direction: column;
    gap: 1.1rem;
}

.footer_conteudo__li__a,
.footer__conteudo__li__a__header {
    text-decoration: none;
    color: #fff;
    font-size: 1rem;
}

.footer__conteudo__li__header {
    display: flex;
    justify-content: space-between;
}

.footer__powered {
    display: flex;
    flex-direction: column;
    align-items: flex-start; 
}

#logo__principal{
    width: 150px;
}

#logo__polgo {
    width: 150px; 
}

@media (max-width: 780px) {

    .footer{
        margin: 0;
        padding-inline: 0;
    }

    .footer__conteudo {
        grid-template-columns: 1fr;
        text-align: center; 
    }

    .footer__powered {
        order: 3; 
        align-items: center; 
        margin-top: 1rem; 
    }

    #logo__principal {
        align-self: center;
    }

    .footer__conteudo__direita{
        margin-block: 2rem;
    }

    .footer__conteudo__li__header{
        display: flex;
        justify-content: center;
        gap: 2rem;
    }

    .footer__conteudo__social{
        margin-block: 2rem;
    }
}
</style>