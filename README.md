<
!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>App de Bateria</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #111;
      color: #eee;
      margin: 0;
      padding: 0;
      opacity: 0;
      animation: fadein 1s forwards;
    }
    @keyframes fadein { to { opacity: 1; } }
    header { background: linear-gradient(90deg, #ff7e5f, #feb47b); padding: 2rem; text-align: center; }
    header h1 { margin: 0; font-size: 2rem; color: #fff; text-shadow: 2px 2px 8px rgba(0,0,0,0.3); }
    header p { font-size: 1.1rem; color: #fff; opacity: 0.9; }
    .content { padding: 1rem; }
    .aulas { display: flex; flex-direction: column; gap: 0.5rem; }
    button {
      padding: 0.5rem 1rem;
      font-size: 1rem;
      border: none;
      border-radius: 5px;
      background: #444;
      color: #eee;
      cursor: pointer;
      transition: background 0.2s, transform 0.2s;
    }
    button:hover { background: #666; transform: scale(1.05); }
    .aula { margin-top: 1rem; }
    iframe { width: 100%; max-width: 560px; height: 315px; border: none; }
    .cartoon { width: 100px; display: block; margin: 0.5rem auto; }
    .info { background: #222; padding: 1rem; border-radius: 8px; margin-top: 1rem; }
  </style>
</head>
<body>
  <header>
    <h1>🎵 Bora Aprender Bateria! 🥁</h1>
    <p>Descubra grooves incríveis e pratique junto com os vídeos!</p>
  </header>
  <div class="content">
    <div class="aulas">
      <button onclick="mostrarAula('groove')">Groove Básico</button>
      <button onclick="mostrarAula('virada')">Virada Simples</button>
      <button onclick="mostrarAula('cristao')">Groove Cristão</button>
      <button onclick="mostrarAula('funk')">Groove Funk</button>
      <button onclick="mostrarAula('samba')">Groove Samba</button>
      <button onclick="mostrarAula('reggae')">Groove Reggae</button>
    </div>
    <div class="aula" id="aula"></div>
  </div>

  <script>
    function mostrarAula(tipo) {
      let conteudo = '';
      if (tipo === 'groove') {
        conteudo = `
          <h2>Groove Básico</h2>
          <p>Este groove básico usa o bumbo no 1 e 3 e a caixa no 2 e 4, formando a base da maioria das músicas pop e rock. Por isso, ele é o ponto de partida para todo baterista iniciante. Pratique lentamente com o metrônomo e aumente a velocidade aos poucos.</p>
          <img class="cartoon" src="https://img.icons8.com/emoji/48/000000/drum-emoji.png" alt="Baterista tocando"/>
          <iframe src="https://www.youtube.com/embed/QxaJYBjsF7g" allowfullscreen></iframe>
          <div class="info">
            <h3>Virada para Groove Básico</h3>
            <p>Exemplo de virada simples para o Groove Básico: toque bumbo e caixa alternados em semicolcheias e finalize com prato crash.</p>
            <h3>Baquetas, Toms e Pratos</h3>
            <p>Baquetas recomendadas: 5A para iniciantes. Tom médio e pratos (hi-hat fechado, crash aberto e ride) criam um som equilibrado.</p>
          </div>
        `;
      } else if (tipo === 'virada') {
        conteudo = `
          <h2>Virada Simples</h2>
          <p>Esta virada simples preenche o fim do compasso e dá dinâmica entre partes da música. Ela aumenta a energia antes da próxima seção. Comece devagar para acertar a coordenação e depois toque junto com a música.</p>
          <img class="cartoon" src="https://img.icons8.com/emoji/48/000000/musical-notes-emoji.png" alt="Baterista virada"/>
          <iframe src="https://www.youtube.com/embed/2WJm6pWTPHQ" allowfullscreen></iframe>
        `;
      } else if (tipo === 'cristao') {
        conteudo = `
          <h2>Groove Cristão</h2>
          <p>Esse groove é tradicional em músicas gospel e worship, com uma levada suave e consistente que dá suporte ao vocal e à melodia. É importante manter a simplicidade e o feeling para que a música brilhe.</p>
          <img class="cartoon" src="https://img.icons8.com/emoji/48/000000/musical-score-emoji.png" alt="Banda tocando"/>
          <iframe src="https://www.youtube.com/embed/T4mKqL5K2VI" allowfullscreen></iframe>
          <div class="info">
            <h3>Virada para Groove Cristão</h3>
            <p>Use viradas simples e espaçadas para não cobrir o vocal. Baquetas 7A são indicadas para uma pegada mais suave e pratos (hi-hat fechado e crash suave) combinam perfeitamente.</p>
          </div>
        `;
      } else if (tipo === 'funk') {
        conteudo = `
          <h2>Groove Funk</h2>
          <p>O groove de funk é cheio de swing e ghost notes que criam uma pegada dançante e marcante. Ele exige controle e dinâmica entre os toques fortes e os toques leves. Trabalhe lentamente e aumente o swing com a prática.</p>
          <img class="cartoon" src="https://img.icons8.com/emoji/48/000000/performing-arts-emoji.png" alt="Baterista tocando funk"/>
          <iframe src="https://www.youtube.com/embed/KvT0IFiJAA8" allowfullscreen></iframe>
          <div class="info">
            <h3>Virada para Groove Funk</h3>
            <p>Adicione viradas com ghost notes e acentuações entre as mãos e o bumbo. Baquetas 5B para maior peso e pratos (ride fechado e crash acentuado) criam o punch necessário para o funk.</p>
          </div>
        `;
      } else if (tipo === 'samba') {
        conteudo = `
          <h2>Groove Samba</h2>
          <p>O samba depende da coordenação entre mãos e pés, com o bumbo marcando a base e a caixa e o chimbal tocando sincopado. O suingue e a independência entre os membros são fundamentais para capturar o balanço brasileiro.</p>
          <img class="cartoon" src="https://img.icons8.com/emoji/48/000000/tropical-drink-emoji.png" alt="Baterista tocando samba"/>
          <iframe src="https://www.youtube.com/embed/JRa3woxUJ8I" allowfullscreen></iframe>
          <div class="info">
            <h3>Virada para Groove Samba</h3>
            <p>Inclua viradas rápidas e sincronizadas entre toms agudos e surdos. Use baquetas 7A para mais agilidade e pratos finos que abrem rápido, mantendo o swing característico do samba.</p>
          </div>
        `;
      } else if (tipo === 'reggae') {
        conteudo = `
          <h2>Groove Reggae</h2>
          <p>O reggae dá ênfase nos contratempos, com um clima relaxado e suave. Trabalhe a marcação fora do tempo e a leveza na pegada para que o groove tenha a vibe típica do estilo caribenho.</p>
          <img class="cartoon" src="https://img.icons8.com/emoji/48/000000/palm-tree-emoji.png" alt="Baterista tocando reggae"/>
          <iframe src="https://www.youtube.com/embed/MldnhsrGvmY" allowfullscreen></iframe>
          <div class="info">
            <h3>Virada para Groove Reggae</h3>
            <p>Adicione viradas leves e espaçosas para o clima relaxado. Baquetas 2B são indicadas para maior peso, e pratos abafados e ride seco reforçam o estilo.</p>
          </div>
        `;
      }
      document.getElementById('aula').innerHTML = conteudo;
    }
  </script>
</body>
</html>
