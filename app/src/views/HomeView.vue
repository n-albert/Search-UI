<script setup>

</script>

<script>
  import router from '../router/index.js';
  export default {
      name: "SearchOptions",
      data() {
          return {
              searchSelection: "",
              textareaInput: "",
              doesRotate: false
          };
      },
      methods: {
          submitSearch() {
              this.doesRotate = true;
              alert(`Hello!`)
              router.push('/results')
          }
      }
  };
</script>

<template>
  <main>
    <header>
      <div class="wrapper">
        <div class="greetings">
          <RouterLink to="/">
            <div :class="{ rotate: doesRotate}"> 
              <img alt="Binoculars from SVGRepo" class="ui-logo" id="uiLogo" src="@/assets/binoculars-svgrepo-com.svg" width="125" height="125" />
            </div>
          </RouterLink>
          <h1 class="green">Search UI</h1>
        </div>
      </div>
    </header>
    <div class="search-options">
        <div>Selected search type: {{ searchSelection }}</div>
        <input type="radio" v-model="searchSelection" id="document-set-one" value="Document Set One" />
        <label for="document-set-one">Document Set One</label><br />

        <input type="radio" v-model="searchSelection" id="document-set-two" value="Document Set Two" />
        <label for="document-set-two">Document Set Two</label><br />
    </div>
    <div class="search-input">
        <span>Multiline message is:</span>
        <p>{{ textareaInput }}</p>
        <textarea v-model="textareaInput" placeholder="add multiple lines"></textarea>
    </div>
    <button @click="submitSearch" :class="{ rotate: doesRotate}">Search</button>
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

.search-input p {
    white-space: pre-line;
}

.search-input textarea {
    width: 512px;
    min-width: 512px;
    min-height: 250px;
}

.rotate {
  rotate: 180deg;
  transition: rotate 2s;
}


@media (min-width: 512px) {
  .greetings h1,
  .greetings span {
    text-align: center;
  }
}
</style>