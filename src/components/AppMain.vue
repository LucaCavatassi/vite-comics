<script>
    export default {
        data() {
        return {

        }
        }
    }
</script>

<template>
    <div class="container">
        <main class="small-wrapper">
            <div> --> Content Goes Here... <-- </div>
        </main>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    .container {
        display: flex;
        justify-content: center;
        background-color: $main-black;
        div {
            padding: 50px 0;
            color: white;
            font-weight: bolder;
            font-size: 1.3rem;
        }
    }
</style>