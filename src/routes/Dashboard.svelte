<style>
    .ticker-item {
        background-color: #0a3555;
        padding: 8px;
        border-radius: 8px;
        margin: 0 0 16px;
    }
    .ticker-item .ticker-header, .ticker-item .ticker-stats {
        display: flex;
        justify-content: space-evenly;
    }
    .ticker-item > div {
        margin: 8px 0;
    }
    .ticker-item .ticker-column {
        margin: 0 8px;
    }
    .ticker-item .ticker-column .column-name {
        font-size: 10px;
    }
    .ticker-item .ticker-column .column-detail {
        font-size: 24px;
    }
    .ticker-item .ticker-graph {
        width: 100%;
        height: 240px;
        background-color: #0d0e10;
        border-radius: 4px;
    }
</style>

<div class="ticker-item">
    <div class="ticker-header">
        <div class="ticker-column">
            <div class="column-name">Symbol</div>
            <div class="column-detail">$DOGE</div>
        </div>
        <div class="ticker-column">
            <div class="column-name">Live Price</div>
            <div class="column-detail clr-bad">$0.058377</div>
        </div>
        <div class="ticker-column">
            <div class="column-name">24 Hour Price</div>
            <div class="column-detail">$0.06422</div>
        </div>
        <div class="ticker-column">
            <div class="column-name">24 Hour Change</div>
            <div class="column-detail clr-bad">-$0.01153</div>
        </div>
    </div>
    <div class="ticker-graph"></div>
    <div class="ticker-stats">
        <div class="ticker-column">
            <div class="column-name">Current Coin</div>
            <div class="column-detail">643.1245</div>
        </div>
        <div class="ticker-column">
            <div class="column-name">Live Value</div>
            <div class="column-detail clr-good">$143.11</div>
        </div>
        <div class="ticker-column">
            <div class="column-name">Avg Paid</div>
            <div class="column-detail clr-good">$0.41345</div>
        </div>
    </div>
</div>