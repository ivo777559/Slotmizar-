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
