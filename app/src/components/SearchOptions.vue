<template>
    <div class="search-options">
        <div>Selected search type: {{ searchSelection }}</div>
        <input type="radio" v-model="searchSelection" id="standards" value="Standards" />
        <label for="standards">Standards</label><br />

        <input type="radio" v-model="searchSelection" id="prodcedures" value="Procedures" />
        <label for="procedures">Procedures</label><br />
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