<h1 style="text-align: center;">📌 Sprint 03</h1>

<table>
  <tbody>
    <tr>
      <td><strong>Capacidade estimada da equipe</strong></td>
      <td>26 Story Points</td>
    </tr>
    <tr>
      <td><strong>Meta da Sprint</strong></td>
      <td>
        Garantir a segurança, persistência e escalabilidade do sistema com autenticação de usuários, histórico de consultas, implantação em ambiente de produção em nuvem e integração com ferramentas GIS externas.
      </td>
    </tr>
    <tr>
      <td><strong>Período</strong></td>
      <td>11/05/2026 – 31/05/2026</td>
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
      <td>20</td>
      <td>Como administrador, quero que o acesso à plataforma exija autenticação para garantir que apenas usuários autorizados utilizem o sistema.</td>
      <td>
        O sistema deve exigir login com e-mail e senha antes do acesso; credenciais inválidas devem bloquear o acesso com mensagem de erro; sessões autenticadas devem ser mantidas com token seguro; rotas protegidas não devem ser acessíveis sem autenticação.
      </td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>21</td>
      <td>Como usuário, quero acessar o histórico das minhas consultas anteriores para retomar análises sem precisar repetir as perguntas.</td>
      <td>
        O sistema deve armazenar cada consulta realizada vinculada ao usuário autenticado; o histórico deve listar consultas com data, pergunta e resumo; ao selecionar uma consulta, o sistema deve reexibir os resultados e o mapa correspondente.
      </td>
      <td>5</td>
    </tr>
    <tr align="center">
      <td>22</td>
      <td>Como equipe, queremos que o sistema esteja implantado em ambiente de produção em nuvem para que esteja disponível de forma estável e escalável.</td>
      <td>
        O sistema deve estar acessível por URL pública; o deploy deve incluir backend, frontend e banco de dados; a aplicação deve suportar múltiplos acessos simultâneos sem falhas; deve haver configuração de variáveis de ambiente e monitoramento básico de disponibilidade.
      </td>
      <td>8</td>
    </tr>
    <tr align="center">
      <td>23</td>
      <td>Como analista GIS, quero consumir as camadas geoespaciais geradas pelo sistema diretamente no QGIS para integrar os dados às minhas análises.</td>
      <td>
        O sistema deve disponibilizar os dados geoespaciais em formatos compatíveis (GeoJSON ou WMS/WFS); deve ser possível carregar as camadas diretamente no QGIS via URL; os dados devem manter geometria, atributos e sistema de coordenadas corretos.
      </td>
      <td>8</td>
    </tr>
  </tbody>
</table>


<h2>Modelo de dados</h2>
<img src="https://github.com/Sync-FATEC/API-2026-6SEM/blob/main/sprints/sprint02/modelo-de-dados.png">
