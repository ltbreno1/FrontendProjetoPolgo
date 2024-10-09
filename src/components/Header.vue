<script>
export default {
  data() {
    return {
      menuActive: false 
    };
  },
  methods: {
    toggleMenu() {
      this.menuActive = !this.menuActive; 
    }
  }
};
</script>

<template>
  <header class="header">
    <div class="header__items">
      <img
        src="https://placehold.jp/f7efd8/ffffff/100x50.png"
        class="header__items__logo"
        alt=""
      />
      <nav class="header__items__navbar">
        <button class="header__items__navbar__toggle" @click="toggleMenu">
          <img id="icone-dropdown" src="../assets/Vector.png" alt="">
        </button>
        <ul class="header__items__navbar__ul" :class="{ active: menuActive }">
          <li class="header__items__navbar__li" v-if="menuActive">
            <img class="header__items__navbar__li__img" src="../assets/imagem-usuário.png" alt="">
            <a class="header__items__navbar__li__a"><b>LOGIN/CADASTRO</b></a>
          </li>
          <li class="header__items__navbar__li">
            <a class="header__items__navbar__li__a" href="">HOME</a>
          </li>
          <li class="header__items__navbar__li">
            <a class="header__items__navbar__li__a" href="">COMO PARTICIPAR</a>
          </li>
          <li class="header__items__navbar__li">
            <a class="header__items__navbar__li__a" href="">PREMIOS</a>
          </li>
          <li class="header__items__navbar__li">
            <a class="header__items__navbar__li__a" href="">DUVIDAS FREQUENTES</a>
          </li>
          <li class="header__items__navbar__li">
            <a class="header__items__navbar__li__a" href="">GANHADORES</a>
          </li>
          <!-- Sempre exibe LOGIN/CADASTRO no final -->
          <li class="header__items__navbar__li" v-if="!menuActive">
            <img class="header__items__navbar__li__img" src="../assets/imagem-usuário.png" alt="">
            <a class="header__items__navbar__li__a"><b>LOGIN/CADASTRO</b></a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    z-index: 1000; 
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    display: flex;
    justify-content: center;
    height: 80px;
}

.header__items {
    display: flex;
    padding-inline: 2rem;
    justify-content: space-between;
    align-items: center;
    background-color: #273142;
    width: 100%;
}

.header__items__logo {
  width: 200px;
  height: 60px;
}

.header__items__navbar {
    display: flex;
    align-items: center;
}

.header__items__navbar__ul {
    display: flex;
    align-items: center;
    list-style-type: none;
    gap: 0 2rem;
}

.header__items__navbar__li {
    display: flex;
    align-items: center;
    gap: 1px;
    margin-inline: .5rem;
}

.header__items__navbar__li__a {
    color: #f7efd8;
    font-size: 1rem;
}

.header__items__navbar__toggle {
    display: none;
    background: none;
    border: none;
    color: #f7efd8;
    font-size: 1.5rem;
    cursor: pointer;
}

@media (max-width: 1520px) {

  .header__items__navbar__ul {
    gap: 0 1rem;
  }

  .header__items {
    padding: 1rem;
  }
}

@media (max-width: 1318px) {
  .header__items__navbar__li__a {
    font-size: 1.1rem;
  }

  .header__items__navbar__ul {
    gap: 0 1rem;
  }

  .header__items {
    padding: 1rem;
  }

  .header__items__navbar__li {
    margin-inline: .5rem;
  }
}

@media (max-width: 1220px) {
  .header__items__navbar__li__a {
    font-size: 1rem;
  }

  .header__items__navbar__li {
    margin-inline: .05rem;
  }

  .header__items__logo{
    width: 158px;
  }
}

@media (max-width: 1024px) {
    .header__items__navbar__ul {
        display: none; 
        flex-direction: column;
        position: absolute;
        background-color: gray;
        top: 70px; 
        left: 0;
        width: 100%;
        padding: 1rem 0;
    }

    .header__items__navbar__ul.active {
        display: flex; 
        background-color: #556270;
        margin-top: .5rem;
    }

    .header__items__navbar__li__a {
      margin-block: 1rem;
    }

    .header__items__navbar__toggle {
        display: block; 
    }

    .header__items__logo {
      width: 158px;
    }
}

</style>
