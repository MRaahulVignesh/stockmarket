<template>
    <div class="about-page-container">
        <div class="about-page-title-container">
            <h2>ABOUT</h2>
        </div>
        <div class="about-page-table-container">
            
        </div>
    </div>
</template>
<script>
  export default {
    data() {
    }
  }
</script>
<style>
    .about-page-container {
        padding: 2rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
        height: 80vh;
        min-height: 600px;
    }

    .about-page-title-container {
        display: flex;
        align-items: top;
        justify-content: center;
        height: 20%;
    }
    
    .about-page-title-container h2 {
        font-size: 3rem;
    }

    .about-page-table-container {
        height: 75%;
        width: 80%;
    }

    @media(max-width: 750px) {
        .stocks-page-container {
            padding: 1rem;
        }

        .stocks-page-title-container {
            height: 10%;
            align-items: center;
        }

        .stocks-page-table-container {
            height: 80%;
        }

        .stocks-page-title-container h2 {
            font-size: 2rem;
        }

        .row-class {
            height: 50px;;
            font-size: 1rem;
        }
    }

</style>