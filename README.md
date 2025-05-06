# Slotmizar-<!DOCTYPE html><html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Slot Mizar - O Poder Cósmico</title>
  <style>
    body {
      background: radial-gradient(circle, #1a1a40, #000);
      color: #fff;
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 50px;
    }
    h1 {
      color: #8ecdfc;
      text-shadow: 0 0 10px #3cf;
    }
    .slot-container {
      display: flex;
      justify-content: center;
      margin: 30px 0;
    }
    .reel {
      background: #222;
      border: 3px solid #8ecdfc;
      border-radius: 10px;
      width: 80px;
      height: 80px;
      margin: 0 10px;
      font-size: 2em;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 0 15px #3cf;
    }
    #spinBtn {
      background: #3cf;
      color: #000;
      border: none;
      padding: 10px 20px;
      font-size: 1.2em;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }
    #spinBtn:hover {
      background: #1a9acb;
    }
    #result {
      margin-top: 20px;
      font-size: 1.5em;
    }
  </style>
</head>
<body>
  <h1>Slot Mizar - O Poder Cósmico</h1>
  <div class="slot-container">
    <div class="reel" id="reel1">?</div>
    <div class="reel" id="reel2">?</div>
    <div class="reel" id="reel3">?</div>
  </div>
  <button id="spinBtn">GIRAR</button>
  <div id="result"></div>  <script>
    const symbols = ['☆', '☀', '⚡', '✨', '✵']; // estrela, sol, raio, brilho, galáxia

    function getRandomSymbol() {
      return symbols[Math.floor(Math.random() * symbols.length)];
    }

    document.getElementById('spinBtn').addEventListener('click', () => {
      const r1 = getRandomSymbol();
      const r2 = getRandomSymbol();
      const r3 = getRandomSymbol();

      document.getElementById('reel1').textContent = r1;
      document.getElementById('reel2').textContent = r2;
      document.getElementById('reel3').textContent = r3;

      if (r1 === r2 && r2 === r3) {
        document.getElementById('result').textContent = 'JACKPOT MIZAR! Você ganhou x10';
      } else if (r1 === r2 || r2 === r3 || r1 === r3) {
        document.getElementById('result').textContent = 'Boa! Duas combinam. x2';
      } else {
        document.getElementById('result').textContent = 'Nada ainda... tente de novo!';
      }
    });
  </script></body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Slot Estelar Mizar</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #1e1e1e;
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
        .slot-machine {
            display: flex;
            justify-content: center;
            margin: 20px;
        }
        .slot {
            width: 100px;
            height: 100px;
            margin: 10px;
            background-color: #222;
            border: 2px solid #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 36px;
            color: #00ff00;
        }
        .controls {
            margin-top: 20px;
        }
        .btn {
            padding: 10px 20px;
            background-color: #00ff00;
            color: black;
            border: none;
            font-size: 18px;
            cursor: pointer;
            margin: 10px;
        }
        .btn:hover {
            background-color: #00cc00;
        }
        .fichas {
            margin-top: 10px;
            font-size: 24px;
        }
        audio {
            display: none;
        }
    </style>
</head>
<body>
    <h1>Slot Estelar Mizar</h1>
    <div class="slot-machine">
        <div class="slot" id="slot1">0</div>
        <div class="slot" id="slot2">0</div>
        <div class="slot" id="slot3">0</div>
    </div>
    <div class="controls">
        <button class="btn" onclick="playGame()">Jogar</button>
        <div class="fichas" id="fichas">Fichas: 100</div>
    </div>
    <audio id="musicaEstelar" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        Seu navegador não suporta o áudio.
    </audio>

    <script>
        let fichas = 100;
        const musicaEstelar = document.getElementById("musicaEstelar");

        function playGame() {
            if (fichas <= 0) {
                alert("Você não tem fichas suficientes!");
                return;
            }
            fichas--;
            document.getElementById("fichas").innerText = "Fichas: " + fichas;
            musicaEstelar.play();

            const slot1 = Math.floor(Math.random() * 10);
            const slot2 = Math.floor(Math.random() * 10);
            const slot3 = Math.floor(Math.random() * 10);

            document.getElementById("slot1").innerText = slot1;
            document.getElementById("slot2").innerText = slot2;
            document.getElementById("slot3").innerText = slot3;

            setTimeout(() => {
                checkResult(slot1, slot2, slot3);
            }, 1000);
        }

        function checkResult(slot1, slot2, slot3) {
            if (slot1 === slot2 && slot2 === slot3) {
                alert("Você ganhou o jackpot! Parabéns!");
                fichas += 50; // Ganho no jackpot
                document.getElementById("fichas").innerText = "Fichas: " + fichas;
            } else {
                alert("Tente novamente!");
            }
        }
    </script>
</body>
</html>
