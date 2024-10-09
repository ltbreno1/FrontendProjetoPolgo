<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css'; 

export default {
  data() {
    return {
      images: [
        "https://placehold.jp/f7efd8/ffffff/360x360.png",
        "https://placehold.jp/f7efd8/ffffff/360x360.png",
        "https://placehold.jp/f7efd8/ffffff/360x360.png",
        "https://placehold.jp/f7efd8/ffffff/360x360.png",
        "https://placehold.jp/f7efd8/ffffff/360x360.png"
      ],
      swiperOptions: {
        breakpoints: {
          320: { slidesPerView: 1, spaceBetween: 40},
          1519: { slidesPerView: 4, spaceBetween: 40}
        }
      }
    };
  },
  components: {
    Swiper,
    SwiperSlide,
  },
};
</script>

<template>
    <section class="section__carrossel">
        <h2 class="section__carrossel__titulo">PREMIOS</h2>
        <div class="section__carrossel__imagens">
            <Swiper
                    :slides-per-view="4"
                    :space-between="100"
                    loop
                    :breakpoints="swiperOptions.breakpoints"
                    class="default-slider"
                >
                    <SwiperSlide v-for="image in images" :key="image">
                    <img id="section__carrossel__imagens" :src="image" alt="" />
                    </SwiperSlide>
             </Swiper>

        </div>
    </section>
    
</template>

<style scoped>

    .section__carrossel{
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        gap: 50px;
    }
    .section__carrossel__titulo{
        color: #666666;
        margin-top: 50px;
    }

    .swiper-horizontal {
        width: 100%;
        max-width: 1520px;
}

@media (max-width: 1518px){

    .section__carrossel__imagens{
      width: 100%;
      max-width: 680px;
    }

    #section__carrossel__imagens{
      width: 100%;
    }

    .swiper-horizontal {
        width: 100%;
        max-width: 680px;
}
}

@media (max-width: 1000px){

.section__carrossel__imagens{
  width: 100%;
  max-width: 550px;
}

#section__carrossel__imagens{
  width: 100%;
}

.swiper-horizontal {
    width: 100%;
    max-width: 550px;
}
}

@media (max-width: 690px){
  .section__carrossel__imagens{
      width: 100%;
      max-width: 360px;
    }

    #section__carrossel__imagens{
      width: 100%;
    }

    .swiper-horizontal {
        width: 100%;
        max-width: 360px;
}
}

@media (max-width: 440px){
  .section__carrossel__imagens{
      width: 100%;
      max-width: 280px;
    }

    #section__carrossel__imagens{
      width: 100%;
    }

    .swiper-horizontal {
        width: 100%;
        max-width: 280px;
}
}

@media (max-width: 380px){
  .section__carrossel__imagens{
      width: 100%;
      max-width: 200px;
    }

    #section__carrossel__imagens{
      width: 100%;
    }

    .swiper-horizontal {
        width: 100%;
        max-width: 200px;
}
}

</style>