<template>
    <div class="uk-container uk-container-large uk-margin-medium-top uk-margin-medium-bottom">

        <div class="uk-position-relative uk-visible-toggle uk-light" tabindex="-1" uk-slider>
            <ul class="uk-slider-items uk-child-width-1-3@s uk-grid">
                <li v-for="(item, index) in items" :key="index">
                    <div
                        class="main-card uk-card uk-card-default uk-margin-medium-bottom uk-margin-medium-top uk-margin-medium-left">
                        <div class="uk-card-body ">
                            <span
                                class="uk-position-top-left uk-label-warning  uk-margin-small-top uk-margin-small-left">
                                {{ item.promo }}
                            </span>
                            <span class="uk-position-top-right uk-margin-small-top uk-margin-right">📩</span>
                            <div class="position-img">
                                <img :src="item.image">
                            </div>
                            <div class="card-img uk-text-center uk-margin-small-top main-txt">
                                {{ item.title }}
                            </div>
                            <div class="uk-text-center uk-margin-small-top">
                                <span class="shipping-card">{{ item.shipping }}</span>
                                <span class="shipping-card uk-margin-left">{{ item.shipping }}</span>
                            </div>
                            <div class="uk-text-center uk-margin-top">
                                <span class="value-txt">A partir de:
                                    <span class="value-txt-bold">
                                        R$ {{ item.value }}
                                    </span>
                                </span>
                            </div>
                            <div class="uk-text-center uk-margin-small-top">
                                <button class="buttom-sec" href="">Comprar</button>
                            </div>
                        </div>
                    </div>
                </li>
            </ul>
            <a class="uk-position-center-right next-previous " href uk-slidenav-next uk-slider-item="next"></a>
        </div>
    </div>

</template>

<script>
import flowers from './flowers.png';

export default {
    data() {
        return {
            items: [
                {
                    title: 'Coroa de Flores BH A',
                    image: flowers,
                    promo: 'Melhor preço',
                    shipping: 'Frete grátis',
                    description: '',
                    value: '000,00',
                },
                {
                    title: 'Coroa de Flores BH A',
                    image: flowers,
                    promo: 'Melhor preço',
                    shipping: 'Frete grátis',
                    description: '',
                    value: '000,00',
                },
                {
                    title: 'Coroa de Flores BH A',
                    image: flowers,
                    promo: 'Melhor preço',
                    shipping: 'Frete grátis',
                    description: '',
                    value: '000,00',
                },
                {
                    title: 'Coroa de Flores BH A',
                    image: flowers,
                    promo: 'Melhor preço',
                    shipping: 'Frete grátis',
                    description: '',
                    value: '000,00',
                },
            ]
        };
    }
};
</script>

<style scoped>
.main-txt {
    color: #59B210;
    font-family: 'Verdana', sans-serif;
    font-size: 16px;
    font-weight: 700;
    line-height: 24px;
    letter-spacing: 0.15000000596046448px;
    text-align: center;


}

.shipping-card {
    background: #E8DEF8;
    border-radius: 100px;
    font-weight: 500;
    font-family: 'Roboto', sans-serif;
    font-size: 14px;
    padding: 5px 25px 5px 25px;
}

.main-card {
    width: 380px;
    border-radius: 16px;
    border-color: black;
    box-shadow: 1px 3px 10px 2px #00000026;
    box-shadow: 1px 3px 10px 2px #0000004D;
}

.uk-label-warning {
    background-color: #FA954B;
    color: white;
    font-family: 'Roboto', sans-serif;
    padding: 6px 16px 6px 16px;
    font-size: 14px;
    border-radius: 8px;
    border: none;
    box-shadow: 0px 1px 3px 1px #00000026;
    box-shadow: 0px 1px 2px 0px #0000004D;
}

.buttom-sec {
    background: #59B210;
    color: white;
    width: 263px;
    border: none;
    padding: 10px, 24px, 10px, 24px;
    font-size: 14px;
    height: 40px;
    border-radius: 100px;


}

.position-img {
    margin-top: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: -10px;
}

.value-txt {
    font-size: 14px;
    font-family: 'Verdana', sans-serif;
    color: #555555;

}

.value-txt-bold {
    font-size: 14px;
    font-family: 'Verdana', sans-serif;
    font-weight: 700;
    color: #1D192B;
}

.next-previous {
    color: #59B210;
}
</style>