<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Darksite - Shop</title>
    <style>
        body {
            background-color: #000; /* Schwarzer Hintergrund */
            color: #0f0; /* Grüne Schrift */
            font-family: "Courier New", Courier, monospace;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        h1 {
            font-size: 2.5em;
            margin: 20px 0;
            text-shadow: 0 0 10px #0f0; /* Glüheffekt */
        }
        p {
            font-size: 1.2em;
        }
        .balance {
            margin-top: 20px;
            font-size: 1.5em;
            color: #ff0;
        }
        .search-box {
            margin: 20px auto;
            padding: 10px;
        }
        input[type="text"] {
            padding: 10px;
            width: 80%;
            font-size: 1em;
            background-color: #333;
            color: #fff;
            border: 1px solid #0f0;
        }
        input[type="submit"] {
            padding: 10px 20px;
            font-size: 1em;
            background-color: #0f0;
            color: #000;
            border: none;
            cursor: pointer;
        }
        .item {
            margin: 20px auto;
            padding: 10px;
            border: 1px solid #0f0;
            width: 80%;
            text-align: left;
            background-color: #111;
        }
        .item img {
            max-width: 100px;
            float: left;
            margin-right: 10px;
        }
        .item button {
            padding: 5px 10px;
            font-size: 0.9em;
            background-color: #0f0;
            color: #000;
            border: none;
            cursor: pointer;
        }
        footer {
            margin-top: 30px;
            font-size: 0.9em;
            color: #888;
        }
        ul {
            text-align: left;
            margin-top: 20px;
            padding-left: 20px;
        }
        ul li {
            font-size: 1.2em;
            margin: 10px 0;
        }
        ul a {
            color: #0f0;
            text-decoration: none;
        }
        ul a:hover {
            text-decoration: underline;
        }
    </style>
    <script>
        let balance = 100; // Startguthaben

        function updateBalance(amount) {
            balance += amount;
            document.getElementById("balance").innerText = `Balance: $${balance} Fake-Geld`;
        }

        function buyItem(price) {
            if (balance >= price) {
                balance -= price;
                alert("Kauf erfolgreich!");
                updateBalance(0);
            } else {
                alert("Nicht genug Fake-Geld!");
            }
        }

        function earnMoney() {
            updateBalance(50);
            alert("Du hast $50 Fake-Geld verdient, indem du Poki besucht hast!");
        }

        function goToPoki() {
            window.location.href = "https://worldbirthsanddeaths.com/"; // Weiterleitung zur Website
        }
    </script>
</head>
<body>
    <h1>Welcome to Darksite</h1>
    <p>Suche nach Artikeln, verdiene Fake-Geld und kaufe etwas!</p>
    <div class="balance" id="balance">Balance: $100 Fake-Geld</div>
    <button onclick="earnMoney()">Verdiene $50 Fake-Geld (besuche Poki.de)</button>

    <!-- Button für die Weiterleitung zur Website -->
    <button onclick="goToPoki()">Besuche Poki.de und verdiene Fake-Geld</button>

    <div class="search-box">
        <form onsubmit="return false;">
            <input type="text" id="search" placeholder="Suche nach Artikeln...">
            <input type="submit" value="Suchen">
        </form>
    </div>

    <div class="item">
        <img src="https://steigerlegal.ch/wp-content/uploads/2024/03/usb-stick-virus-002.jpeg" alt="Item 1">
        <h3>Artikel 1: Fake-USB-Stick</h3>
        <p>Preis: $30 Fake-Geld</p>
        <button onclick="buyItem(30)">Kaufen</button>
    </div>

    <div class="item">
        <img src="https://images.thalia.media/-/BF2000-2000/fd4d066fe2d249258c37e5b0144d4997/einfuehrung-ins-darknet-taschenbuch-martin-hoffer.jpeg" alt="Item 2">
        <h3>Artikel 2: Hacker-Buch</h3>
        <p>Preis: $50 Fake-Geld</p>
        <button onclick="buyItem(50)">Kaufen</button>
    </div>

    <div class="item">
        <img src="https://i.etsystatic.com/46123051/r/il/e84154/5197439686/il_1080xN.5197439686_3vwn.jpg" alt="Item 3">
        <h3>Artikel 3: Mysteriöse Box</h3>
        <p>Preis: $80 Fake-Geld</p>
        <button onclick="buyItem(80)">Kaufen</button>
    </div>

    <!-- Liste der gruseligen Websites -->
    <div>
        <h2>Gruselige Websites:</h2>
        <ul>
            <li><a href="https://www.rentahitman.com" target="_blank">Rent-a-Hitman</a></li>
            <li><a href="https://www.playhitman.com/" target="_blank">Hitman Simulator</a></li>
            <li><a href="https://www.planecrashinfo.com/" target="_blank">PlaneCrashInfo</a></li>
            <li><a href="https://www.tdcj.texas.gov/death_row/dr_executed_offenders.html" target="_blank">Death Row Information</a></li>
            <li><a href="https://thebulletin.org/doomsday-clock/" target="_blank">Doomsday Clock</a></li>
            <li><a href="https://deadfake.com/" target="_blank">Dead Fake</a></li>
            <li><a href="http://www.joyofsatan.org/" target="_blank">The Joy of Satan</a></li>
            <li><a href="https://thepurgatory.net/" target="_blank">The Purgatory</a></li>
            <li><a href="http://www.simulation-argument.com/" target="_blank">Simulation Argument</a></li>
            <li><a href="https://dyingwordsproject.com/" target="_blank">Dying Words</a></li>
        </ul>
    </div>

    <footer>
        <p>Darksite - Hidden in plain sight.</p>
    </footer>
</body>
</html>
