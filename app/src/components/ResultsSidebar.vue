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
    <div class="results-sidebar">
        <h3>This is the sidebar, where filters or other features would appear.</h3>
    </div>
</template>

<style>
    .results-sidebar {
        height: 500px;
        width: 250px;
        border-right: dashed rgb(0, 147, 59);
    }
</style>