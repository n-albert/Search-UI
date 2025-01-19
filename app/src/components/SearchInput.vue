<script>
   import router from '../router/index.js';

    export default {
        name: "searchInput",
        data() {
            return {
                textareaInput: "",
            };
        },
        methods: {
            submitSearch() {
                /* alert(`Hello!`) */
                router.push('/results')
            }
        }
    };
</script>

<template>
    <div class="search-input">
        <span>Multiline message is:</span>
        <p>{{ textareaInput }}</p>
        <textarea v-model="textareaInput" placeholder="add multiple lines"></textarea>
    </div>
    <button @click="submitSearch">Search</button>
</template>


<style>
    .search-input p {
        white-space: pre-line;
    }

    .search-input textarea {
        width: 512px;
        min-width: 512px;
        min-height: 250px;
    }
</style>