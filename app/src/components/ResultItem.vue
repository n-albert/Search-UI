<script>
    export default {
        data() {
            return {
            showContent: false
    };
  }
};
</script>

<template>
    <div class="result-card">
        <div class="result-banner" @click="showContent = !showContent">

        </div>

        <div class="result-content-default">

        </div>
        <div class="result-content-expanded" v-if="showContent">

        </div>
    </div>
</template>

<style>

.result-card {
    flex: 1;
    flex-flow: column;
    margin: 25px 25px 0px 25px;
    border: rgb(181, 247, 207);
}

.result-banner {
    background-color: darkolivegreen;
    flex: 1;
    height: 30px;
}

.result-content-default {
    background-color: rgb(181, 247, 207);
    height: 110px
}

.result-content-expanded {
    background-color: rgb(181, 247, 207);
    height: 110px
}

</style>