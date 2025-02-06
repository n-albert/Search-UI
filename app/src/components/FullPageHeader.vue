<script>
    import router from '../router/index.js';
    import { RouterLink } from 'vue-router';

    export default {
      name: "SearchOptions",
      data() {
          return {
              rotateClicked: false,
              rotationDuration: 500
          };
      },
      methods: {
          rotation() {
            this.rotateClicked = !this.rotateClicked;
            setTimeout(() => this.rotateClicked = !this.rotateClicked, this.rotationDuration)
            setTimeout(() => router.push('/'), 750)
          }
      }
  };
</script>

<template>
    <div class="full-page-header">
        <div class="logo-div" @click="rotation" :class="{ rotateClicked }">
            <img alt="Binoculars from SVGRepo" class="ui-logo" id="uiLogo" src="@/assets/binoculars-svgrepo-com.svg"/>
        </div>   
        <h3 class="green">Search Results</h3>
    </div>
</template>

<style scoped>
.full-page-header {
    width: 100%; 
    flex-direction: row;
    padding-top: 0px;
    padding-bottom: 20px;
    vertical-align: auto;
    border-bottom: double rgb(0, 147, 59);

}

.logo-div {
    width: 60px;
    height: 60px;
    float: left;
    margin-right: 25px;
}

.green {
    float: left;
    font-weight: 500;
    font-size: 2.6rem;
    line-height: normal;
    padding: 0 rem;
}

.full-page-header h1,
.full-page-header span {
  text-align: left;
}

.rotateClicked {
  transform: rotate(360deg);
  transition: transform 500ms ease-in-out;
  
}

@media (min-width: 512px) {
  .full-page-header h1,
  .full-page-header span {
    text-align: left;
  }
}
</style>