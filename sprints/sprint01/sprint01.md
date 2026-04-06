<h1 style="text-align: center;">📌 Sprint 01</h1>

<table>
  <tbody>
    <tr>
      <td><strong>Capacidade estimada da equipe</strong></td>
      <td>63 Story Points</td>
    </tr>
    <tr>
      <td><strong>Meta da Sprint</strong></td>
      <td>Entregar a base funcional do sistema: consulta de imóvel rural via CAR, visualização no mapa interativo, integração com fontes públicas de dados ambientais e chat com linguagem natural com rastreabilidade de fontes.</td>
    </tr>
    <tr>
      <td><strong>Período</strong></td>
      <td>16/03/2026 – 05/04/2026</td>
    </tr>
  </tbody>
</table>

<h2>Backlog da Sprint</h2>

<table>
  <thead>
    <tr align="center">
      <th>Rank</th>
      <th>User Story</th>
      <th>Critério de Aceitação</th>
      <th>Estimativa</th>
    </tr>
  </thead>
  <tbody>
    <tr align="center">
      <td>1</td>
      <td>Como usuário, quero informar o código de uma propriedade rural para que eu possa consultar suas informações geográficas.</td>
      <td>O sistema aceita o código CAR e retorna os dados da propriedade correspondente; exibe mensagem de erro caso o código não seja encontrado.</td>
      <td>3</td>
    </tr>
    <tr align="center">
      <td>2</td>
      <td>Como usuário, quero visualizar a propriedade rural no mapa para entender sua localização e dimensão.</td>
      <td>O polígono da propriedade é exibido no mapa com base no GeoJSON retornado pelo SICAR; o mapa centraliza automaticamente na área consultada.</td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>3</td>
      <td>Como usuário, quero visualizar informações básicas da propriedade para compreender seu contexto inicial.</td>
      <td>O sistema exibe nome do município, área em hectares, status (ativo/pendente/suspenso) e módulos fiscais da propriedade consultada.</td>
      <td>3</td>
    </tr>
    <tr align="center">
      <td>4</td>
      <td>Como usuário, quero interagir com o mapa (zoom, navegação e clique) para explorar a propriedade.</td>
      <td>O mapa suporta zoom, pan e clique em elementos; ao clicar em um ponto do mapa, exibe as informações do registro correspondente.</td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>5</td>
      <td>Como usuário, quero visualizar diferentes camadas ambientais no mapa para entender o contexto geográfico da propriedade.</td>
      <td>O mapa exibe camadas de queimadas, desmatamento (DETER/PRODES), terras indígenas, unidades de conservação e comunidades quilombolas; cada camada pode ser ativada ou desativada independentemente.</td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>6</td>
      <td>Como usuário, quero que o sistema utilize dados públicos integrados de diferentes fontes para garantir análises completas.</td>
      <td>O sistema consome e armazena dados do INPE/Queimadas, INPE/DETER, INPE/PRODES, FUNAI, ICMBio, Fundação Cultural Palmares e SICAR/CAR; os dados são indexados no corpus semântico via pgvector.</td>
      <td>8</td>
    </tr>
    <tr align="center">
      <td>7</td>
      <td>Como administrador, quero atualizar a base de dados manualmente para garantir que o sistema utilize informações recentes.</td>
      <td>O sistema disponibiliza um botão de atualização da base; ao acioná-lo, o pipeline ETL é executado; o sistema exibe status da execução (em andamento, sucesso ou erro) e registra logs da atualização.</td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>8</td>
      <td>Como sistema, quero atualizar automaticamente os dados em intervalos definidos para manter a base sempre atualizada.</td>
      <td>O sistema executa automaticamente o pipeline ETL em intervalos configuráveis (ex: diário); a execução não interrompe o uso do sistema; evita duplicação de dados e registra logs de cada execução.</td>
      <td>8</td>
    </tr>
    <tr align="center">
      <td>9</td>
      <td>Como usuário, quero fazer perguntas em linguagem natural para obter informações sobre queimadas, desmatamento, terras indígenas, unidades de conservação, comunidades quilombolas e imóveis rurais no Estado de São Paulo.</td>
      <td>O chat aceita perguntas em português e retorna resposta com resumo textual, dados estruturados e pontos no mapa para cada domínio suportado; perguntas fora do escopo retornam mensagem explicativa.</td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>10</td>
      <td>Como usuário, quero que o sistema identifique automaticamente a intenção da minha pergunta para que eu receba a resposta correta sem precisar seguir um formato rígido.</td>
      <td>O classificador (Naive Bayes + TF-IDF treinado com 214 exemplos) identifica a intenção correta com confiança ≥ 0,3 para perguntas dentro do escopo; o sistema faz pré-processamento com tokenização, remoção de stopwords e stemming.</td>
      <td>8</td>
    </tr>
    <tr align="center">
      <td>11</td>
      <td>Como usuário, quero receber um resumo textual junto com os pontos no mapa para entender de onde vieram os dados retornados.</td>
      <td>Cada resposta do chat inclui: resumo em português com quantidade de registros encontrados e localização, lista de dados com metadados e GeoJSON com os pontos plotados no mapa.</td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>12</td>
      <td>Como usuário, quero visualizar a fonte de cada dado retornado (INPE, FUNAI, ICMBio, Palmares, SICAR) para garantir rastreabilidade das análises.</td>
      <td>Cada resposta exibe a lista de fontes utilizadas com nome e identificador; os dados no mapa contêm o campo "fonte" em suas propriedades GeoJSON.</td>
      <td>3</td>
    </tr>
  </tbody>
</table>

<h2>Modelo de dados</h2>
<img src="https://github.com/Sync-FATEC/API-2026-6SEM/blob/main/sprints/sprint01/modelo-de-dados.png">

<h2>MVP</h2>
<img src="https://github.com/Sync-FATEC/API-2026-6SEM/assets/cf2ae83f-9e76-4ac0-8cf0-48ea02134a28" 
alt="MVP">
