<template>
    <div class="uk-container uk-container-large">
        <nav class="main-nav">
            <div uk-navbar>
                <div class="uk-navbar-left">
                    <img :src="LogoImageUrl">
                </div>
                <div class="uk-navbar-right">
                    <ul class="uk-navbar-nav">
                        <li v-for="(item, index) in menuItems" :key="index">
                            <a :href="item.link" class="menu-item uk-margin-left ">{{ item.text }}</a>
                        </li>
                    </ul>
                    <button class="login-button">Login</button>
                </div>
            </div>
        </nav>
    </div>
    <div class="uk-subnav-backgr uk-container uk-container-expand">
        <h1 class="main-title-2">Frete grátis e faixa de homenagem sem custo - compre pelo <a href="">WhatsApp</a></h1>
    </div>
    <div class="uk-background-cover uk-img-background" :data-src="backgroundImage" uk-img>
        <div class="uk-container uk-container-large">
            <div class="uk-text-position">
                <h1 class="main-title">
                    <span class="main-title-span">Qualidade e preço baixo</span>
                    em um<br>
                    só Lugar!
                    Confira os <span class="main-title-span">melhores preços<br> </span>em Belo Horizonte e região.
                </h1>
            </div>
            <button class="button-primary uk-margin-medium-top">Conferir</button>
        </div>
    </div>
</template>
<script>
import logoImg from './logomarca.png';
import backgroundImage from './backgroundImageUrl.png';

export default {
    name: 'HeaderComponent',
    data() {
        return {
            LogoImageUrl: logoImg,
            backgroundImage: backgroundImage,
            menuItems: [
                { text: 'Home', link: '#' },
                { text: 'Quem Somos', link: '#' },
                { text: 'Coroas', link: '#' },
                { text: 'Frases de Homenagem', link: '#' },
            ],
        };
    },
};
</script>
<style scoped>

:root {
  --primary-color: #59B210;
  --secondary-color: #244906;
  --background-color: #F5EFF7;
  --text-color: #DBF9C2;
}

.main-nav {
    background-color: white;
}

.login-button {
    font-family: 'Roboto', sans-serif;
    padding: 10px 24px 10px 24px;
    border-radius: 20px;
    border: none;
    background-color: #59B210;
    color: white;
    cursor: pointer;
}

.button-primary {
    font-family: 'Roboto', sans-serif;
    padding: 10px 50px 10px 50px;
    font-size: 18px;
    border-radius: 20px;
    border: none;
    background-color: #59B210;
    color: white;
    cursor: pointer;
}

.uk-img-background {
    height: 600px;
    max-width: 100%;
}

.uk-subnav-backgr {
    background-color: #F5EFF7;
}

.uk-text-position {
    margin-top: 180px;
}

.main-title {
    color: #DBF9C2;
    font-family: 'Verdana', sans-serif;
    font-size: 35px;
    font-weight: 400;
    line-height: 40px;
    text-align: left;
}

.main-title-span {
    font-weight: 800;
    color: white;
    font-size: 34px;
}

.main-title-2 {
    font-family: 'Verdana', sans-serif;
    font-size: 14px;
    font-weight: 400;
    line-height: 20px;
    letter-spacing: 0.10000000149011612px;
    text-align: center;
    padding: 10px;

}

.menu-item {
    font-family: 'Roboto', sans-serif;
    text-transform: none;
    font-size: 16px;
    font-weight: 400;
    line-height: 24px;
    letter-spacing: 0.5px;
    text-align: center;
    color: #244906;
}


@media only screen and (max-width: 800px) {}
</style>