<template>
    <div class="container">
      <div class="uk-container uk-container-large">
        <div class="uk-position-relative uk-visible-toggle uk-light" tabindex="-1" uk-slider>
          <ul class="uk-slider-items uk-child-width-1-3@s uk-grid">
            <li v-for="(item, index) in items" :key="index">
              <div class="main-card uk-card uk-card-default uk-margin-medium-left">
                <div class="uk-card-body">
                  <div class="card-img uk-text-center">
                    {{ item.title }}
                  </div>
                </div>
              </div>
            </li>
          </ul>
          <a class="uk-position-center-right next-previous" href uk-slidenav-next uk-slider-item="next"></a>
          <ul class="uk-slider-nav uk-dotnav uk-flex-center uk-margin"></ul>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import imgBack from './background.png';
  
  export default {
    data() {
      return {
        items: [
          { title: 'Coroa de Flores BH A' },
          { title: 'Coroa de Flores BH B' },
          { title: 'Coroa de Flores BH C' },
          { title: 'Coroa de Flores BH D' },
        ],
        backgroundimg: imgBack,
      };
    },
  };
  </script>
  
  <style scoped>
  .container {
    background-image: url('./background.png');
    background-size: cover;
    min-height: 500px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .main-card {
    width: 380px;
    border-radius: 16px;
    border-color: black;
    box-shadow: 1px 3px 10px 2px #00000026;
    box-shadow: 1px 3px 10px 2px #0000004D;
  }
  </style>
  