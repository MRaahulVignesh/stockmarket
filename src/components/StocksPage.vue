<template>
    <div class="stocks-page-container">
        <div class="stocks-page-title-container">
            <h2>MARKET TREND</h2>
        </div>
        <div class="stocks-page-table-container">
            <b-table hover sticky-header="400px" borderless :items="items" tbody-tr-class="row-class" thead-class="head-class">
                <template #table-caption>Note: The Prices are dynamically updated for every 5 seconds.</template>
            </b-table>
            
        </div>
    </div>
</template>
<script>
// const WebSocket = require('ws');
  export default {
    mounted() {
        const ws = new WebSocket('wss://api.tiingo.com/crypto');
        const subscribe = {
            'eventName':'subscribe',
            'authorization':'49e2c7e36d82837974ba356e39f66a34fc1915bf',
            'eventData': {
                'thresholdLevel': 5
            }
        }

        ws.on('open', function open() {
            ws.send(JSON.stringify(subscribe));
        });

        ws.on('message', function(data) {
            console.log(data)
        });

    },
    data() {
      return {
        fields: ['Name', 'Last Price'],
        items: [
          { name: "Ethereum", last_price: '$300', day_change: '0.12%'},
          { name: "Bitcoin", last_price: '$450', day_change: '1.46%'},
          { name: "Bitcash", last_price: '$645232', day_change: '1.02%'},
          { name: "Neocoin", last_price: '$31236', day_change: '0.95%'},
          { name: "Ethereum", last_price: '$300', day_change: '0.12%'},
          { name: "Bitcoin", last_price: '$450', day_change: '1.46%'},
        ]
      }
    }
  }
</script>
<style>
    .stocks-page-container {
        padding: 2rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
        height: 80vh;
        min-height: 600px;
    }

    .stocks-page-title-container {
        display: flex;
        align-items: top;
        justify-content: center;
        height: 20%;
    }
    
    .stocks-page-title-container h2 {
        font-size: 3rem;
    }

    .stocks-page-table-container {
        height: 75%;
        width: 80%;
    }

    .row-class  {
        height: 75px;
        font-weight: bold;
        color: black;
        font-size: 1.25rem;
        text-align: left;
        padding: 1rem;
    } 
    .head-class  {
        color: rgb(226, 14, 14);
        text-align: left;
        font-size: 0.8rem;
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