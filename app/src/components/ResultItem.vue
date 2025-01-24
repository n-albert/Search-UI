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
            <div v-if="showContent" class="result-content-expanded" >
                <div class="result-secondary-content-container">

                </div>
            </div>
    </div>
</template>

<style>

.result-card {
    flex: 1;
    flex-direction: column;
    margin: 25px 25px 0px 25px;
    border: rgb(181, 247, 207);
}

.result-banner {
    background-color: rgb(26, 117, 84);
    flex: 1;
    height: 30px;
}

.result-content-default {
    background-color: rgb(34, 185, 130);
    height: 110px
}

.result-content-expanded {
    background-color: rgb(34, 185, 130);
    height: 110px;
    flex-direction: column;
    align-items: center;

}

.result-secondary-content-container {
    background-color: rgb(206, 212, 210);
    margin-left: auto;
    margin-right: auto;
    min-width: 90%;
    max-width: fit-content;
    height: 85px;
}

</style>