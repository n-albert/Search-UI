<template>
    <div class="search-options-container">
        <div>Selected search type: {{ searchSelection }}</div>
        <div class="search-options">    
            <div class="search-option" :class="{ 'selected': searchSelection === 'Document Set One' }">
                <input type="radio" v-model="searchSelection" id="document-set-one" value="Document Set One" />
                <label for="document-set-one">Document Set One</label><br />
            </div>
            <div class="search-option" :class="{ 'selected': searchSelection === 'Document Set Two' }">
                <input type="radio" v-model="searchSelection" id="document-set-two" value="Document Set Two" />
                <label for="document-set-two">Document Set Two</label><br />
            </div>      
        </div>
    </div>
</template>

<script>
    export default {
        name: "SearchOptions",
        data() {
            return {
                searchSelection: "",
            };
        },
    };
</script>

<style>
    .search-options-container {
        min-height: 50px;
        margin-top: 20px;
        margin-bottom: 20px;
    }
    .search-options {
        display: flex;
    }
    .search-option {
        width: 150px;
        height: 25px;
        border: 2px solid gray;
        text-align: center;
    }

    .search-option input {
        opacity: 0;
    }

    .search-option label {
        position: relative;
        left: -6.5px;
    }

    .selected {
        background-color: rgb(0, 189, 126);
        color: black;
    }
</style>