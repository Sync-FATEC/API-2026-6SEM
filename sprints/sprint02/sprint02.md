
<h1 style="text-align: center;">📌 Sprint 02</h1>

<table>
  <tbody>
    <tr>
      <td><strong>Capacidade estimada da equipe</strong></td>
      <td>45 Story Points</td>
    </tr>
    <tr>
      <td><strong>Meta da Sprint</strong></td>
      <td>
    Evoluir o sistema com detecção de múltiplas intenções em uma única consulta, cruzamento contextual entre imóvel rural e dados ambientais, cálculo de nota de risco ASG, exportação de relatório em PDF, disponibilização de dashboard com indicadores socioambientais, implementação de retentativas automáticas em caso de falha na obtenção de dados e controle da atualização de bases com visualização de status por fonte.
      </td>
    </tr>
    <tr>
      <td><strong>Período</strong></td>
      <td>13/04/2026 – 03/05/2026</td>
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
      <td>13</td>
      <td>Como usuário, quero combinar dois temas em uma única pergunta (ex: "queimadas e unidades de conservação em Ubatuba") para obter respostas integradas sem precisar fazer consultas separadas.</td>
      <td>
        O sistema detecta até 2 intenções secundárias via keywords e probabilidade do classificador (limiar ≥ 0,10); retorna resultados mesclados de cada fonte no mesmo GeoJSON; o resumo da resposta indica a contagem por tipo de dado encontrado.
      </td>
      <td>8</td>
    </tr>
    <tr align="center">
      <td>14</td>
      <td>Como analista, quero que o sistema cruze os dados de um imóvel rural (CAR) com alertas de queimadas e desmatamento na mesma região para identificar automaticamente se a propriedade está associada a passivos ambientais.</td>
      <td>
        Ao consultar um imóvel pelo código CAR, o sistema verifica a ocorrência de queimadas (INPE), alertas DETER e polígonos PRODES dentro ou no entorno da propriedade; os registros encontrados são exibidos no mapa como camadas sobrepostas ao polígono do imóvel; a resposta indica quais passivos foram identificados.
      </td>
      <td>8</td>
    </tr>
    <tr align="center">
      <td>15</td>
      <td>Como usuário, quero visualizar uma nota de risco socioambiental de 0 a 100 da propriedade consultada, calculada com base nos dados de desmatamento, queimadas e interseções com áreas protegidas, para apoiar a tomada de decisão.</td>
      <td>
        O sistema calcula e exibe a nota de risco ASG (0 = sem risco, 100 = risco máximo) com base em: número de focos de queimada, área desmatada (DETER/PRODES) e interseção com terras indígenas, unidades de conservação e comunidades quilombolas; a nota é exibida no chat e no relatório junto com os fatores que a compõem.
      </td>
      <td>8</td>
    </tr>
    <tr align="center">
      <td>16</td>
      <td>Como usuário, quero exportar o resultado da análise em PDF contendo o resumo, os dados e o mapa para compartilhar ou arquivar o relatório.</td>
      <td>
        O botão de exportação gera um PDF com: título da consulta, data, resumo textual, nota de risco ASG, tabela de dados retornados com fonte e imagem estática do mapa com os pontos plotados; o arquivo é baixado diretamente pelo navegador.
      </td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>17</td>
      <td>Como usuário, quero acessar uma aba de dashboard com indicadores visuais para entender rapidamente a situação socioambiental das propriedades analisadas.</td>
      <td>
        O sistema exibe uma aba "Dashboard" com gráficos e indicadores como: quantidade de propriedades analisadas, média da nota de risco ASG, total de áreas com desmatamento e queimadas; os dados são atualizados dinamicamente conforme as consultas realizadas
      </td>
      <td>3</td>
    </tr>
     <tr align="center">
      <td>18</td>
      <td>Como usuário, quero que o sistema tente novamente automaticamente quando ocorrer erro na obtenção de dados, para garantir que falhas momentâneas de instabilidade não impactem minha análise.</td>
      <td>
      O sistema deve realizar novas tentativas automáticas apenas em casos de falha de comunicação com fontes externas, limitando-se a no máximo 4 tentativas adicionais, com intervalos controlados entre cada tentativa.
      </td>
      <td>8</td>
    </tr>
    <tr align="center">
      <td>19</td>
      <td>Como usuário, quero escolher quais bases de dados desejo atualizar e visualizar o status de cada atualização, para ter controle sobre o processo e entender se houve sucesso ou erro em cada fonte.</td>
      <td>
      O sistema deve permitir que o usuário selecione uma ou mais bases de dados para atualização, exibindo o status individual de cada base durante ou após a execução, além de apresentar mensagens claras e compreensíveis em caso de falha.
      </td>
      <td>5</td>
    </tr>
  </tbody>
</table>

<h2>Modelo de dados</h2>
<img src="https://github.com/Sync-FATEC/API-2026-6SEM/blob/main/sprints/sprint02/modelo-de-dados.png">
