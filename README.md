<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Bem-vinda ao nosso diário!</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />
  <link href="https://fonts.googleapis.com/css2?family=Gloria+Hallelujah&display=swap" rel="stylesheet" />
  <style>
    body {
      font-family: 'Gloria Hallelujah', cursive;
      background-color: #0b0c2a;
      background-image: radial-gradient(ellipse at bottom, #0b0c2a 0%, #000000 100%);
      color: #FFFFFF;
      margin: 0;
      padding: 0;
      text-align: center;
      transition: background-color 0.3s ease, color 0.3s ease;
      overflow-x: hidden;
      position: relative;
    }

    .stars {
      width: 2px;
      height: 2px;
      background: white;
      position: absolute;
      border-radius: 50%;
      animation: twinkle 2s infinite;
      opacity: 0.8;
    }

    @keyframes twinkle {
      0%, 100% { opacity: 0.8; }
      50% { opacity: 0.2; }
    }

    .stars:nth-child(n) {
      animation-delay: calc(0.1s * var(--i));
    }

    .moon {
      position: fixed;
      top: 30px;
      left: 30px;
      width: 40px;
      height: 40px;
      background: radial-gradient(circle at 30% 30%, #fff, #ccc);
      border-radius: 50%;
      box-shadow: 0 0 40px 10px #ffffff44;
      z-index: 1;
    }

    .comet {
      position: fixed;
      top: 100px;
      left: -200px;
      width: 120px;
      height: 4px;
      background: linear-gradient(to right, #fff, rgba(255, 255, 255, 0));
      transform: rotate(-45deg);
      animation: moveComet 8s linear infinite;
      z-index: 1;
    }

    @keyframes moveComet {
      0% { left: -200px; top: 100px; opacity: 1; }
      70% { opacity: 1; }
      100% { left: 120%; top: -100px; opacity: 0; }
    }

    .button {
      background-color: #FFD700;
      color: #003A66;
      border: none;
      padding: 10px 20px;
      margin: 15px;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      font-family: 'Gloria Hallelujah', cursive;
      transition: transform 0.2s;
    }

    .button:hover {
      transform: scale(1.05);
    }

    .letter-style {
      background-color: #fffaf0;
      color: #333;
      padding: 25px;
      border-radius: 15px;
      max-width: 600px;
      margin: 0 auto;
      font-family: 'Gloria Hallelujah', cursive;
      box-shadow: 0 5px 20px rgba(255, 255, 255, 0.2);
      border: 2px solid #f5deb3;
      line-height: 1.7;
      font-size: 18px;
    }

    table {
      margin: 20px auto;
      border-collapse: collapse;
      width: 80%;
      background-color: #2a2b44;
      border-radius: 10px;
      overflow: hidden;
    }

    th, td {
      padding: 10px;
      text-align: center;
      border: 1px solid #fff;
    }

    th {
      background-color: #FFD700;
      color: #003A66;
    }

    td {
      color: #fff;
    }
  </style>
</head>
<body>
  <!-- Estrelas -->
  <div class="stars" style="top:5%; left:10%; --i:1;"></div>
  <div class="stars" style="top:10%; left:25%; --i:2;"></div>
  <div class="stars" style="top:20%; left:80%; --i:3;"></div>
  <div class="stars" style="top:25%; left:60%; --i:4;"></div>
  <div class="stars" style="top:40%; left:30%; --i:5;"></div>
  <div class="stars" style="top:45%; left:90%; --i:6;"></div>
  <div class="stars" style="top:60%; left:70%; --i:7;"></div>
  <div class="stars" style="top:75%; left:50%; --i:8;"></div>
  <div class="stars" style="top:80%; left:10%; --i:9;"></div>
  <div class="stars" style="top:85%; left:40%; --i:10;"></div>

  <div class="moon"></div>
  <div class="comet"></div>

  <header>
    <h1>✨ Bem-vinda ao nosso diário mágico ✨</h1>
    <h2>💌 Um novo capítulo da nossa história 💌</h2>
  </header>

  <button onclick="toggleTheme()" class="button" style="position: absolute; top: 20px; right: 20px;">🌙 / ☀️</button>

  <section>
    <div class="highlighted-section">🌟 Fomos na final da Superliga! 🌟</div>

    <div class="interest">
      <h3>🏐 Vimos o retorno do minas e agora: A queda!</h3>
      <p>Elas não queriam ir pra final, mas você acabou levando boa parte delas pro ginásio.</p>
    </div>

    <div class="interest">
      <h3>🎓 Semana de provas: Você consegue!</h3>
      <p>Você tá entrando na primeira semana de provas, e imagino como deva estar preocupada, com medo e talvez até duvidando de você mesma, e é normal se sentir assim. Só saiba que não está sozinha pra passar por tudo isso! 🍀</p>
    </div>

    <div class="interest">
      <h3>🤔 Fim de temporada de clubes, vem brilhar seleção.</h3>
      <p>Você me prometeu que a temporada de seleção é boa e estou ansiosa pra acompanhar com você. Palpites pra VNL?</p>
    </div>

    <div class="interest">
      <h3>🗕️ Acho que 500 roles até setembro vai ser meio apertado.</h3>
      <p>Mas que ir tomar um café comigo depois de um dia difícil?</p>
    </div>

    <button class="button" onclick="playSong()">🎶 Atualizamos a trilha sonora! Tocar Jão - "Supernova"!</button>
        <div id="audio-container">
            <iframe id="audio-player" src="https://www.youtube.com/watch?v=31BeluA7dRE"></iframe>

      <!-- Spotify -->
      <div style="margin-top: 20px;">
        <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/6yi8xpwomPTO1UyfTj7FyG" width="100%" height="152" frameborder="0" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
      </div>
    </div>

    <button class="button" onclick="showSpecialMessage()">💌 Mensagem especial do mês</button>
    <div id="special-message" class="animate__animated" style="display:none;">
      <p>Você é uma das pessoas mais fortes que já conheci, mesmo com tanta coisa pra dar conta, não tenha medo dos seus sonhos e continue lutando pelo que acredita.  🌈✨</p>
    </div>

    <button class="button" onclick="showLoveLetter()">💖 Uma carta só pra você</button>
    <div id="love-letter" class="animate__animated" style="display: none; margin-top: 20px;">
      <div class="letter-style">
        <p>
          Assim como o Jão escreveu uma carta por show, dessa vez eu queria fazer uma coisa parecida e além de atualizar o diário, conseguir me expressar um pouco mais. <br /><br />
          Não sei se o universo planejou, se foi sorte ou só um daqueles encontros raros, mas desde o dia da fila do show, eu me sinto muito feliz por ter conhecido você.<br /><br />
          Me encanta tua leveza, tua inteligência, esse jeito doce e seguro de estar no mundo (mesmo quando sente medo). Gosto do silêncio confortável entre a gente, das conversas sobre esporte, a vida, faculdade, e até dos nossos planos meio malucos que a gente vai criando no improviso. <br /><br />
          Queria que soubesse que você tem sido um abrigo bonito nesses dias incertos. E mais que isso — tem sido inspiração, espero poder ser abrigo para você um dia e te deixar confortável pra falar comigo sobre o que precisar<br /><br />
          Se esse diário é um retrato de nós, então que ele seja eterno enquanto for sincero e sem pressa pra ser escrito. <br /><br />
          Com carinho, admiração e um sorriso bobo no rosto,<br />
          <strong>— de mim, pra você 💌</strong>
        </p>
      </div>
    </div>

    <!-- Tabela dos jogos da seleção brasileira de vôlei feminino em junho de 2025 -->
    <h3>📅 Próximos Jogos da Seleção Brasileira de Vôlei Feminino - Junho 2025</h3>
    <table>
      <thead>
        <tr>
          <th>Data</th>
          <th>Competição</th>
          <th>Oponente</th>
          <th>Horário</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>04/06/2025</td>
          <td>Liga das Nações</td>
          <td> Repúblia Tcheca</td>
          <td>17h30</td>
        </tr>
        <tr>
          <td>05/06/2025</td>
          <td>Liga das Nações</td>
          <td>EUA</td>
          <td>21h00</td>
        </tr>
        <tr>
          <td>07/06/2025</td>
          <td>Liga das Nações</td>
          <td>Alemanha</td>
          <td>13h30</td>
        </tr>
        <tr>
          <td>08/06/2025</td>
          <td>Liga das Nações</td>
          <td>Italia</td>
          <td>10h00</td>
        </tr>
      </tbody>
    </table>
  </section>

  <footer>
    <p>&copy; 2025 Nosso Diário - Com carinho, sempre 💖</p>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
  <script>
    function showSpecialMessage() {
      const msg = document.getElementById("special-message");
      msg.style.display = "block";
      msg.classList.add("animate__fadeInUp");
    }

    function showLoveLetter() {
      const letter = document.getElementById("love-letter");
      letter.style.display = "block";
      letter.classList.add("animate__fadeInUp");
    }

    function playSong() {
      const player = document.getElementById("audio-player");
      const currentSrc = player.src;
      player.src = '';
      setTimeout(() => player.src = currentSrc, 100);
    }
  </script>
</body>
</html>



