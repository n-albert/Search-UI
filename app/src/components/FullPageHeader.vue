<script>
   import router from '../router/index.js';
   import { RouterLink } from 'vue-router';
</script>

<template>
    <div class="full-page-header">
        <div class="logo-div">
            <RouterLink to="/">
                <img alt="Binoculars from SVGRepo" class="ui-logo" id="uiLogo" src="@/assets/binoculars-svgrepo-com.svg"/>
            </RouterLink>
        </div>   
        <h3 class="green">Search Results</h3>
    </div>
</template>

<style scoped>
.full-page-header {
    width: 100%; 
    flex-direction: row;
    padding-top: 20px;
    padding-bottom: 20px;
    vertical-align: auto;
    border-bottom: double rgb(0, 147, 59);

}

.logo-div {
    width: 60px;
    height: 60px;
    float: left;
}

.green {
    float: left;
    font-weight: 500;
    font-size: 2.6rem;
    line-height: normal;
}

.full-page-header h1,
.full-page-header span {
  text-align: left;
}

@media (min-width: 512px) {
  .full-page-header h1,
  .full-page-header span {
    text-align: left;
  }
}
</style>