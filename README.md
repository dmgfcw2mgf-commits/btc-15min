<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#070912">

<title>BTC15 AI</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    background:
        radial-gradient(circle at 50% -10%, #182653 0%, #070912 45%);
    color: #f2f5ff;
    font-family:
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        sans-serif;
}

.app {
    max-width: 520px;
    margin: auto;
    padding: 16px 14px 35px;
}

/* HEADER */

.header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 15px;
}

.brand {
    display: flex;
    align-items: center;
    gap: 10px;
}

.logo {
    width: 42px;
    height: 42px;
    border-radius: 13px;

    display: flex;
    align-items: center;
    justify-content: center;

    font-size: 23px;
    font-weight: 900;

    background:
        linear-gradient(135deg, #8b7cff, #36d8ff);

    box-shadow:
        0 0 30px rgba(100, 100, 255, .35);
}

.brand-title {
    font-size: 18px;
    font-weight: 850;
}

.brand-subtitle {
    font-size: 11px;
    color: #8e99af;
    margin-top: 2px;
}

.live {
    color: #39e58c;
    border: 1px solid rgba(57,229,140,.3);
    background: rgba(57,229,140,.08);

    padding: 6px 9px;
    border-radius: 20px;

    font-size: 11px;
}

/* MAIN CARD */

.hero {
    background:
        linear-gradient(145deg, #11182a, #0b0f19);

    border: 1px solid #202a40;
    border-radius: 24px;

    padding: 18px;

    box-shadow:
        0 20px 60px rgba(0,0,0,.45);
}

.market-row {
    display: flex;
    justify-content: space-between;

    color: #8e99af;
    font-size: 12px;
}

.price {
    font-size: 38px;
    font-weight: 900;
    letter-spacing: -1px;

    margin-top: 8px;
}

.change {
    margin-top: 3px;
    font-size: 13px;
    color: #39e58c;
}

/* SIGNAL */

.signal {
    margin-top: 20px;

    text-align: center;

    padding: 20px;

    border-radius: 20px;

    background:
        linear-gradient(135deg, #102c23, #0e1b21);

    border: 1px solid rgba(57,229,140,.35);
}

.signal.down {
    background:
        linear-gradient(135deg, #30131d, #151018);

    border-color:
        rgba(255,92,122,.35);
}

.signal.wait {
    background:
        linear-gradient(135deg, #211b3c, #111525);

    border-color:
        rgba(124,108,255,.45);
}

.signal-word {
    font-size: 32px;
    font-weight: 950;
    letter-spacing: 2px;
}

.signal-probability {
    font-size: 18px;
    margin-top: 5px;
}

.signal-description {
    color: #8e99af;
    font-size: 11px;
    margin-top: 7px;
}

/* GRID */

.grid {
    display: grid;
    grid-template-columns: 1fr 1fr;

    gap: 10px;

    margin-top: 12px;
}

.card {
    background: rgba(13,18,32,.9);

    border:
        1px solid #202a40;

    border-radius: 18px;

    padding: 14px;
}

.label {
    color: #8e99af;
    font-size: 10px;
}

.value {
    font-size: 20px;
    font-weight: 850;

    margin-top: 5px;
}

.edge {
    color: #47d9ff;
}

.meter {
    height: 6px;

    margin-top: 10px;

    background: #20283a;

    border-radius: 10px;

    overflow: hidden;
}

.meter-fill {
    height: 100%;

    width: 0%;

    background:
        linear-gradient(
            90deg,
            #7c6cff,
            #47d9ff
        );

    border-radius: 10px;

    transition:
        width .5s ease;
}

/* SIGNALS */

.section {
    margin-top: 14px;
}

.section-title {
    font-size: 13px;
    margin-bottom: 8px;
}

.signal-row {
    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 12px 0;

    border-bottom:
        1px solid #182033;
}

.signal-row:last-child {
    border-bottom: none;
}

.signal-name {
    font-size: 12px;
}

.signal-value {
    font-size: 12px;
    font-weight: 800;
}

.green {
    color: #39e58c;
}

.red {
    color: #ff5c7a;
}

/* CHART */

.chart {
    height: 120px;

    display: flex;
    align-items: end;

    gap: 3px;

    padding-top: 10px;
}

.bar {
    flex: 1;

    min-height: 8px;

    border-radius:
        5px 5px 2px 2px;

    background:
        linear-gradient(
            #7468ff,
            #2d9cff
        );

    opacity: .9;
}

/* FOOTER */

.footer {
    text-align: center;

    color: #68738a;

    font-size: 10px;

    margin-top: 18px;

    line-height: 1.5;
}

/* NAVIGATION */

.navigation {
    position: sticky;

    bottom: 10px;

    margin-top: 15px;

    display: flex;
    justify-content: space-around;

    padding: 10px;

    border:
        1px solid #283249;

    border-radius: 18px;

    background:
        rgba(11,16,28,.9);

    backdrop-filter:
        blur(18px);
}

.navigation button {
    background: none;
    border: none;

    color: #7f8ba2;

    font-size: 11px;
}

.navigation button.active {
    color: white;
}

/* DESKTOP */

@media (min-width: 700px) {

    body {
        padding-top: 30px;
    }

}
</style>
</head>

<body>

<div class="app">

    <!-- HEADER -->

    <div class="header">

        <div class="brand">

            <div class="logo">
                ₿
            </div>

            <div>

                <div class="brand-title">
                    BTC15 AI
                </div>

                <div class="brand-subtitle">
                    Kalshi 15-minute intelligence
                </div>

            </div>

        </div>

        <div class="live">
            ● LIVE
        </div>

    </div>


    <!-- MAIN -->

    <div class="hero">

        <div class="market-row">

            <span>
                KXBTC15M
            </span>

            <span id="timer">
                15:00
            </span>

        </div>


        <div
            class="price"
            id="btcPrice"
        >
            $108,000.00
        </div>


        <div
            class="change"
            id="btcChange"
        >
            ↗ +0.00%
        </div>


        <!-- AI SIGNAL -->

        <div
            class="signal wait"
            id="signalBox"
        >

            <div
                class="signal-word"
                id="signal"
            >
                WAIT
            </div>

            <div
                class="signal-probability"
                id="probability"
            >
                Model warming up
            </div>

            <div class="signal-description">
                Waiting for enough market data
            </div>

        </div>


        <!-- STATS -->

        <div class="grid">

            <div class="card">

                <div class="label">
                    MODEL PROBABILITY
                </div>

                <div
                    class="value"
                    id="modelProbability"
                >
                    --
                </div>

                <div class="meter">

                    <div
                        class="meter-fill"
                        id="modelMeter"
                    ></div>

                </div>

            </div>


            <div class="card">

                <div class="label">
                    KALSHI PRICE
                </div>

                <div
                    class="value"
                    id="kalshiPrice"
                >
                    --
                </div>

                <div class="meter">

                    <div
                        class="meter-fill"
                        id="kalshiMeter"
                    ></div>

                </div>

            </div>


            <div class="card">

                <div class="label">
                    EDGE
                </div>

                <div
                    class="value edge"
                    id="edge"
                >
                    --
                </div>

            </div>


            <div class="card">

                <div class="label">
                    CONFIDENCE
                </div>

                <div
                    class="value"
                    id="confidence"
                >
                    LOW
                </div>

            </div>

        </div>

    </div>


    <!-- MARKET SIGNALS -->

    <div class="section card">

        <div class="section-title">
            Market Signals
        </div>


        <div class="signal-row">

            <span class="signal-name">
                1 minute momentum
            </span>

            <span
                class="signal-value green"
                id="momentum1"
            >
                --
            </span>

        </div>


        <div class="signal-row">

            <span class="signal-name">
                5 minute momentum
            </span>

            <span
                class="signal-value green"
                id="momentum5"
            >
                --
            </span>

        </div>


        <div class="signal-row">

            <span class="signal-name">
                Trend strength
            </span>

            <span
                class="signal-value"
                id="trend"
            >
                --
            </span>

        </div>


        <div class="signal-row">

            <span class="signal-name">
                Order book
            </span>

            <span
                class="signal-value"
                id="orderBook"
            >
                --
            </span>

        </div>


        <div class="signal-row">

            <span class="signal-name">
                Distance to target
            </span>

            <span
                class="signal-value"
                id="distance"
            >
                --
            </span>

        </div>

    </div>


    <!-- MOMENTUM -->

    <div class="section card">

        <div class="section-title">
            Live Momentum
        </div>

        <div
            class="chart"
            id="chart"
        ></div>

    </div>


    <div class="footer">

        BTC15 AI Research Dashboard<br>

        Paper-trading recommended until the model is validated.

    </div>


    <!-- NAVIGATION -->

    <div class="navigation">

        <button class="active">
            Dashboard
        </button>

        <button>
            Markets
        </button>

        <button>
            History
        </button>

        <button>
            Settings
        </button>

    </div>

</div>


<script>

/*
====================================================
BTC15 AI
FRONT-END DASHBOARD

IMPORTANT:

This version uses DEMO DATA.

It is NOT connected to live Kalshi data yet.

The next version will connect:

Kalshi
+
CF Benchmarks
+
BTC exchange feeds
+
Machine-learning model
====================================================
*/


const $ = id =>
    document.getElementById(id);


/* RANDOM DEMO DATA */

function updateDemo() {

    const btc =
        108000 +
        (Math.random() * 2500 - 1250);


    const direction =
        Math.random() > .5
        ? "UP"
        : "DOWN";


    const probability =
        55 +
        Math.random() * 25;


    const kalshi =
        45 +
        Math.random() * 25;


    const edge =
        probability -
        kalshi;


    /* PRICE */

    $("btcPrice").textContent =
        "$" +
        btc.toLocaleString(
            "en-US",
            {
                minimumFractionDigits: 2,
                maximumFractionDigits: 2
            }
        );


    /* CHANGE */

    const change =
        (Math.random() * .25)
        .toFixed(2);


    $("btcChange").textContent =
        direction === "UP"
        ? "↗ +" + change + "%"
        : "↘ -" + change + "%";


    $("btcChange").className =
        direction === "UP"
        ? "change green"
        : "change red";


    /* SIGNAL */

    let signal =
        "WAIT";


    if (probability >= 65) {

        signal = "UP";

    }

    else if (probability <= 35) {

        signal = "DOWN";

    }


    $("signal").textContent =
        signal;


    $("probability").textContent =
        probability.toFixed(1)
        + "% probability";


    $("signalBox").className =
        "signal "
        +
        signal.toLowerCase();


    /* MODEL */

    $("modelProbability").textContent =
        probability.toFixed(1)
        + "%";


    $("modelMeter").style.width =
        probability
        + "%";


    /* KALSHI */

    $("kalshiPrice").textContent =
        kalshi.toFixed(1)
        + "¢";


    $("kalshiMeter").style.width =
        kalshi
        + "%";


    /* EDGE */

    $("edge").textContent =
        (edge >= 0 ? "+" : "")
        +
        edge.toFixed(1)
        +
        " pts";


    /* CONFIDENCE */

    if (probability >= 72) {

        $("confidence").textContent =
            "HIGH";

    }

    else if (probability >= 62) {

        $("confidence").textContent =
            "MEDIUM";

    }

    else {

        $("confidence").textContent =
            "LOW";

    }


    /* MOMENTUM */

    const m1 =
        (Math.random() * .10)
        .toFixed(2);


    const m5 =
        (Math.random() * .25)
        .toFixed(2);


    $("momentum1").textContent =
        direction === "UP"
        ? "↗ +" + m1 + "%"
        : "↘ -" + m1 + "%";


    $("momentum5").textContent =
        direction === "UP"
        ? "↗ +" + m5 + "%"
        : "↘ -" + m5 + "%";


    /* TREND */

    $("trend").textContent =
        Math.floor(
            40 +
            Math.random() * 55
        )
        +
        "/100";


    /* ORDER BOOK */

    $("orderBook").textContent =
        direction === "UP"
        ? "Bullish"
        : "Bearish";


    /* DISTANCE */

    $("distance").textContent =
        (direction === "UP"
        ? "+"
        : "-")
        +
        (0.05 +
        Math.random() * .30)
        .toFixed(2)
        +
        "%";


    /* CHART */

    const chart =
        $("chart");


    chart.innerHTML =
        "";


    for (
        let i = 0;
        i < 35;
        i++
    ) {

        const bar =
            document.createElement("div");


        bar.className =
            "bar";


        bar.style.height =
            (
                10 +
                Math.random() *
                100
            )
            +
            "px";


        chart.appendChild(
            bar
        );

    }

}


/* COUNTDOWN */

let seconds =
    15 * 60;


function countdown() {

    seconds--;


    if (seconds <= 0) {

        seconds =
            15 * 60;

    }


    const minutes =
        Math.floor(
            seconds / 60
        );


    const secs =
        seconds % 60;


    $("timer").textContent =
        String(minutes)
        .padStart(2,"0")
        +
        ":"
        +
        String(secs)
        .padStart(2,"0");

}


/* START */

updateDemo();


setInterval(
    updateDemo,
    2500
);


setInterval(
    countdown,
    1000
);

</script>

</body>
</html>