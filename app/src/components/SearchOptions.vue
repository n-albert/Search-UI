<template>
    <div class="search-options-container">
        <div>Selected search type: {{ searchSelection }}</div>
        <div class="search-options">    
            <div class="search-option" :class="{ 'selected': searchSelection === 'Standards' }">
                <input type="radio" v-model="searchSelection" id="standards" value="Standards" />
                <label for="standards">Standards</label><br />
            </div>
            <div class="search-option" :class="{ 'selected': searchSelection === 'Procedures' }">
                <input type="radio" v-model="searchSelection" id="procedures" value="Procedures" />
                <label for="procedures">Procedures</label><br />
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