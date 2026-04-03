<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Golf Pot</title>
    <style>
        body { font-family: sans-serif; background: #f0f4f0; display: flex; justify-content: center; padding: 20px; }
        .card { background: white; padding: 25px; border-radius: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); width: 100%; max-width: 350px; }
        h1 { color: #2e7d32; text-align: center; }
        label { display: block; margin-top: 15px; font-weight: bold; }
        input { width: 100%; padding: 12px; margin-top: 5px; border: 1px solid #ccc; border-radius: 8px; box-sizing: border-box; font-size: 16px; }
        button { width: 100%; padding: 15px; margin-top: 20px; border: none; border-radius: 8px; font-size: 18px; font-weight: bold; cursor: pointer; }
        .btn-start { background: #2e7d32; color: white; }
        .btn-winner { background: #ffc107; color: black; margin-bottom: 10px; }
        .hidden { display: none; }
        .result-item { display: flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px solid #eee; font-size: 18px; }
        .win { color: #2e7d32; font-weight: bold; }
        .loss { color: #c62828; font-weight: bold; }
    </style>
</head>
<body>

    <!-- SCREEN 1: SETUP -->
    <div id="setup-screen" class="card">
        <h1>⛳ Golf Pot</h1>
        <label>Number of Players</label>
        <input type="number" id="num-players" value="4">
        <label>Stake per Hole ($)</label>
        <input type="number" id="stake" value="5">
        <label>Total Holes</label>
        <input type="number" id="num-holes" value="18">
        <button class="btn-start" onclick="startGame()">Start Round</button>
    </div>

    <!-- SCREEN 2: PLAYING -->
    <div id="game-screen" class="card hidden">
        <h1 id="hole-display">Hole 1</h1>
        <p style="text-align:center">Who won this hole?</p>
        <div id="player-buttons"></div>
    </div>

    <!-- SCREEN 3: RESULTS -->
    <div id="result-screen" class="card hidden">
        <h1>Final Results</h1>
        <div id="results-list"></div>
        <button class="btn-start" onclick="location.reload()">New Game</button>
    </div>

    <script>
        let players = [];
        let stake = 0;
        let totalHoles = 0;
        let currentHole = 1;

        function startGame() {
            const n = parseInt(document.getElementById('num-players').value);
            stake = parseFloat(document.getElementById('stake').value);
            totalHoles = parseInt(document.getElementById('num-holes').value);

            if (n < 2) { alert("Need at least 2 players"); return; }

            for (let i = 1; i <= n; i++) {
                players.push({ name: "Player " + i, balance: 0 });
            }

            document.getElementById('setup-screen').classList.add('hidden');
            document.getElementById('game-screen').classList.remove('hidden');
            renderGame();
        }

        function renderGame() {
            document.getElementById('hole-display').innerText = "Hole " + currentHole + " / " + totalHoles;
            const container = document.getElementById('player-buttons');
            container.innerHTML = '';

            players.forEach((p, index) => {
                const btn = document.createElement('button');
                btn.className = 'btn-winner';
                btn.innerText = p.name;
                btn.onclick = () => recordWinner(index);
                container.appendChild(btn);
            });
        }

        function recordWinner(winnerIdx) {
            const pot = stake * players.length;
            players.forEach((p, i) => {
                p.balance -= stake;
                if (i === winnerIdx) p.balance += pot;
            });

            if (currentHole < totalHoles) {
                currentHole++;
                renderGame();
            } else {
                showResults();
            }
        }

        function showResults() {
            document.getElementById('game-screen').classList.add('hidden');
            document.getElementById('result-screen').classList.remove('hidden');
            const list = document.getElementById('results-list');
            list.innerHTML = '';

            // Sort: highest money to lowest
            const sorted = [...players].sort((a, b) => b.balance - a.balance);

            sorted.forEach(p => {
                const div = document.createElement('div');
                div.className = 'result-item';
                const colorClass = p.balance >= 0 ? 'win' : 'loss';
                const sign = p.balance >= 0 ? '+' : '';
                div.innerHTML = `<span>${p.name}</span><span class="${colorClass}">${sign}$${p.balance.toFixed(2)}</span>`;
                list.appendChild(div);
            });
        }
    </script>
</body>
</html>
