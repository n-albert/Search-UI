<script setup>
    import ResultItem from './ResultItem.vue';

    defineProps({
        msg: {
            type: String,
            required: true,
        },
    })
</script>

<script>

    /* update this to something else, maybe functions for filters? */
    export default {
        name: "SearchOptions",
        data() {
            return {
                searchSelection: "",
            };
        },
    };
</script>

<template>
    <div class="results-content">
        <ResultItem />
        <ResultItem />
        <ResultItem />
    </div>
</template>

<style>
    .results-content {
        flex: 1;
        flex-wrap: wrap;
        height: auto;
        border-right: dashed rgb(0, 147, 59);
    }
    .results-content h1 {
        padding: 10px 23px 0px 23px;
    }
</style>