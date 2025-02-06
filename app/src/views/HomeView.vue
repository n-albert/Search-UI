<script setup>
  import SearchOptions from '@/components/SearchOptions.vue';
</script>

<script>
  import router from '../router/index.js';
  export default {
      name: "SearchOptions",
      data() {
          return {
              searchSelection: "",
              textareaInput: "",
              rotateClicked: false,
              rotationDuration: 500
          };
      },
      methods: {
          rotation() {
            this.rotateClicked = !this.rotateClicked;
            setTimeout(() => this.rotateClicked = !this.rotateClicked, this.rotationDuration)
          },
          submitSearch() {
              this.rotateClicked = !this.rotateClicked;
              setTimeout(() => router.push('/results'), 750)

          },
      }
  };
</script>

<template>
  <main>
    <header>
      <div class="wrapper">
        <div class="greetings">
          
            <div @click="rotation" :class="{ rotateClicked }"> 
              <img alt="Binoculars from SVGRepo" class="ui-logo" id="uiLogo" src="@/assets/binoculars-svgrepo-com.svg" width="125" height="125" />
            </div>
          <!-- <RouterLink to="/">
          </RouterLink> -->
          <h1 class="green">Search UI</h1>
        </div>
      </div>
    </header>
    <SearchOptions></SearchOptions>
    <!--
    <div class="search-options">
        <div>Selected search type: {{ searchSelection }}</div>
        <input type="radio" v-model="searchSelection" id="document-set-one" value="Document Set One" />
        <label for="document-set-one">Document Set One</label><br />

        <input type="radio" v-model="searchSelection" id="document-set-two" value="Document Set Two" />
        <label for="document-set-two">Document Set Two</label><br />
    </div>
    -->

    <div class="search-input">
        <span>Multiline message is:</span>
        <p>{{ textareaInput }}</p>
        <textarea v-model="textareaInput" placeholder="add multiple lines"></textarea>
    </div>
    <button @click="submitSearch()">Search</button>
  </main>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: center;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings {
  flex: auto;
  align-items: center;
  text-align: center;
}

.greetings h1,
.greetings span {
  text-align: center;
}

.search-options {
  padding-top: 5px;
  padding-bottom: 5px;
}

.search-options label {
  padding-left: 10px;
}

.search-input p {
    white-space: pre-line;
}

.search-input textarea {
    width: 512px;
    min-width: 512px;
    min-height: 250px;
}

.rotateClicked {
  transform: rotate(360deg);
  transition: transform 500ms ease-in-out;
  
}

@media (min-width: 512px) {
  .greetings h1,
  .greetings span {
    text-align: center;
  }
}
</style>