<template>
    <div class="home-container">
    <div class="title-container">
        <div class = "title">
            <h2>
                Crypto in Seconds!
            </h2>
            <h6>Add and Analyze cryptos in no time</h6>
            <b-button variant="warning" class="title-button">Read More</b-button>
        </div>
    <div class="tagline">
    </div>
    </div>
    <div class="logo-container">
        <img src="../assets/title3.png" alt="">
    </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
    .home-container {
        background-image: url('../assets/background.jpeg');
        background-position: center;
        background-size: cover;
        height: 80vh;
        max-height: 750px;
        margin: 0 auto;
        display: flex;
        justify-content: space-around;
    }

    .title-container {
        width: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .logo-container {
        width: 30%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .logo-container img {
        width: 75%;
        background-position: center;
    }

    .title {
        text-align: left;
    }

    .title h2 {
        color: rgb(255, 129, 71);
        font-size: 4rem;
    }

    .title h6 {
        color: rgb(250, 250, 250);
        font-size: 1rem;
    }

    .title-button {
        margin-top: 0.5rem;
    }

    @media(max-width: 750px) {
        .home-container {
            height: 50vh;
            min-height: 500px;
            flex-direction: column-reverse;
            justify-content: center;
            align-items: center;
        }

        .title-container {
            width: 100%;
            justify-content: center;
            align-items: center;
            margin-top: 1rem;
        }

        .logo-container {
            width: 60%;
            padding: 1rem;
        }

        .title {
            text-align: center;
        }

        .logo-container img {
            width: 75%;
            background-position: center;
            max-width: 200px;
            min-width: 100px;
        }

        .title h2 {
            color: rgb(255, 129, 71);
            font-size: 2rem;
        }

        .title h6 {
            color: rgb(250, 250, 250);
            font-size: 1rem;
        }
    }

</style>