1) **Cenários de Interação**

**Cenário de Análise/Problema – Ana**

Monitoramento em Tempo Real e Gerenciamento de Sensores
Atores: Ana Silva (funcinária do INPE)

Ana Silva, analista ambiental do Instituto Nacional de Pesquisas Espaciais (INPE), inicia seu dia acessando o painel de monitoramento de queimadas fornecido pelo programa Queimadas, que utiliza medições por satélite para identificar focos de calor em todo o território nacional. Seu trabalho consiste em validar os registros e emitir relatórios sobre as áreas afetadas.

Durante o monitoramento, Ana percebe que um dos sensores de uma região crítica não envia dados há mais de 25 minutos, sem que o sistema exiba qualquer notificação automática sobre a interrupção. Para confirmar se o problema está no sensor ou na comunicação, ela precisa cruzar manualmente as informações com outros painéis e bases de dados, o que torna o processo lento e propenso a falhas humanas.

Além disso, Ana enfrenta dificuldades devido aos dados chegarem com atraso de tempo, o que prejudica a detecção precoce e a resposta imediata a incêndios florestais. Além disso, as condições meteorológicas, como a presença de nuvens, podem comprometer a visibilidade e dificultar a identificação precisa dos focos.

Outro desafio é a ausência de alertas automáticos em tempo real. Ana precisa verificar manualmente as atualizações no painel, o que demanda atenção constante e aumenta a possibilidade de que ocorrências críticas passem despercebidas. A falta de fácil integração dos sensores ao sistema também torna o processo de validação mais lento.

Assim, o cenário evidencia as limitações das ferramentas atuais baseadas apenas em satélites, que, embora úteis para o monitoramento macro, não atendem plenamente à necessidade de agilidade, precisão e autonomia exigida no combate a queimadas em tempo real.

**Questões de Refinamento:**

| **Índice** | **Elemento**     | **Pergunta**                                                   | **Resposta**                                                                                                                                                                                                |
| :--------: | :--------------- | :------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     [1]    | **Objetivo**     | Qual é o propósito principal da atividade descrita no cenário? | Garantir o monitoramento em tempo real das queimadas e a confiabilidade dos dados enviados pelos sensores do sistema, possibilitando uma resposta rápida em casos de incêndio.                   |
|     [2]    | **Ambiente**     | Em que contexto e local o sistema é utilizado?                 | O sistema é acessado pelo computador da estação de monitoramento do INPE, em um ambiente de controle com conexão constante à rede LoRa e ao servidor local que sincroniza os dados com o painel do Grafana. |
|     [3]    | **Ator(es)**     | Quem interage diretamente com o sistema?                       | Ana, funcionária do INPE, responsável pelo acompanhamento dos sensores, análise de dados ambientais e emissão de relatórios de risco de fogo.                                                               |
|     [4]    | **Planejamento** | O que o ator pretende realizar ao acessar o sistema?           | Ana pretende verificar o status dos sensores ativos, analisar regiões com possíveis focos de incêndio, confirmar alertas e gerar relatórios automáticos para a equipe de campo.                             |
|     [5]    | **Ação**         | Quais são as principais ações realizadas pelo ator?            | Acessar o painel, visualizar o mapa com sensores, verificar alertas de temperatura elevada, tentar reconectar sensores inativos e personalizar o painel para incluir novos gráficos e métricas.  |
|     [6]    | **Evento**       | Que situação inesperada ou problema ocorre durante o uso?      | Durante o monitoramento, Ana percebe que um dos sensores parou de enviar dados há mais de 25 minutos, o que pode indicar falha na comunicação ou desconexão do dispositivo.                                 |
|     [7]    | **Avaliação**    | Como o ator avalia o resultado de suas ações?                  | Após realizar a reconexão remota com sucesso e atualizar o painel, Ana confirma que os dados voltaram a ser exibidos corretamente, avaliando o sistema como eficiente, confiável e fácil de usar.           |


**Nome do Cenário:** Monitoramento em Tempo Real e Gerenciamento de Sensores

**Atores:** Ana Silva (funcionária do INPE)

Ana Silva é uma funcionária do Instituto Nacional de Pesquisas Espaciais (INPE) [3], responsável pelo acompanhamento do sistema Boitatá-II, uma plataforma que integra sensores LoRa, algoritmos de análise de risco e um painel no Grafana.
Seu objetivo é garantir o monitoramento em tempo real dos focos de calor e gerenciar os sensores distribuídos em campo [1].

Durante a manhã, Ana acessa o sistema a partir do computador de sua estação no centro de monitoramento ambiental [2]. Ela inicia seu planejamento verificando o painel principal do Grafana, que apresenta um mapa interativo com as localizações dos sensores e suas respectivas leituras de temperatura e umidade [4].

Em poucos minutos, o painel exibe um alerta visual em vermelho indicando que um dos sensores parou de enviar dados há 25 minutos [6]. Ana decide abrir o menu de gerenciamento e tenta uma reconexão remota com o dispositivo. Enquanto o sistema processa a solicitação, ela observa as métricas do gráfico de temperatura e as últimas leituras recebidas.

Após alguns segundos, o alerta desaparece e o ponto do sensor volta a exibir dados atualizados. Ana confirma a estabilidade do dispositivo e registra no relatório interno o horário de reconexão e o status do sensor. Ela avalia o processo como ágil e intuitivo, destacando que o sistema oferece boa usabilidade e permite o controle remoto sem necessidade de suporte técnico [7].

Ao final do turno, Ana gera um relatório consolidado do dia, exportando gráficos e registros de alertas resolvidos para análise posterior pela equipe de pesquisa.



2) **Design Centrado na Comunicação**

**Nome do Cenário: Monitoramento em Tempo Real e Gerenciamento de Sensores**

| **Tópico > Subtópico (diálogo)**       | **Falas e Signos**                                                                                                                                                                                                                                                                                                                                                                       |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Login no sistema Boitatá-II**        | **U:** Preciso acessar o sistema para iniciar o monitoramento em tempo real.<br>**D:** Informe seu usuário e senha cadastrados no painel.<br>**U:** Digito as credenciais e clico em “Entrar”.<br>**D:** Acesso concedido. Redirecionando para o painel principal de monitoramento.                                                                                                      |
| **Visualizar sensores ativos no mapa** | **U:** Quero ver todos os sensores ativos e suas temperaturas.<br>**D:** No painel do Grafana, cada ponto no mapa representa um sensor. Ao clicar, são exibidas informações de temperatura, umidade e status de conexão.<br>**U:** Clico no sensor identificado como “Sensor_013”.<br>**D:** Exibindo dados do sensor: Temperatura 46°C, Status: Conectado, Última leitura há 2 minutos. |
| **Detectar falha na comunicação**      | **U:** Percebo que um dos sensores não está atualizando há mais de 20 minutos.<br>**D:** O ponto referente ao sensor “Sensor_021” está em vermelho, indicando falha de comunicação. Deseja tentar reconectar o dispositivo?<br>**U:** Sim, clico em “Tentar Reconexão”.                                                                                                                  |
| **Executar ação de reconexão**         | **D:** Reconectando dispositivo... Aguardando resposta do sensor.<br>**U:** Aguardo alguns segundos e atualizo o painel.<br>**D:** Sensor reconectado com sucesso. Última leitura registrada há 1 minuto.                                                                                                                                                                                |
| **Registrar evento e avaliação**       | **U:** Desejo registrar o problema e a reconexão bem-sucedida.<br>**D:** Preencha o campo “Descrição do Evento” e clique em “Salvar Registro”.<br>**U:** Registro concluído. Agora posso gerar o relatório diário.<br>**D:** Relatório exportado com sucesso. Dados prontos para análise e arquivamento.                                                                                 |


3) **Mapa de Objetivos**
> **_NOTE:_**: cada um coloca seu mapa de objetivos e deverá ter um diagrama de consolidação

4) **Esquema Conceitual de Signos**

| **Signo**                 | **Origem** | **Observações**                                           | **Tipo de Conteúdo**              | **Restrições sobre o Conteúdo**              | **Valor Default**                   | **Prevenção (PP)**                            | **Recuperação (RA)**                                         |
| :------------------------ | :--------- | :-------------------------------------------------------- | :-------------------------------- | :------------------------------------------- | :---------------------------------- | :-------------------------------------------- | :----------------------------------------------------------- |
| **Login no sistema**      | Sistema    | Tela inicial de autenticação de usuário                   | Interação de usuário (formulário) | Requer nome de usuário e senha válidos       | Campos vazios                       | PP: Bloqueia login se campos estiverem vazios | RA: Mensagem de erro e tentativa novamente                   |
| **Mapa de Sensores**      | Sistema    | Painel interativo com pontos georreferenciados            | Comportamento do sistema          | Requer conexão com servidor ativo            | Exibe pontos padrão em cinza        | PP: Alerta se algum sensor estiver offline    | RA: O sistema tenta reconectar automaticamente               |
| **Reconexão remota**      | Sistema    | Ação manual ou automática de reconexão com sensor inativo | Comportamento do sistema          | Disponível apenas para usuários autenticados | Botão “Tentar Reconexão” habilitado | PP: Solicita confirmação antes de executar    | RA: Mensagem “Reconexão concluída” ou “Falha na comunicação” |
| **Relatório de evento**   | Usuário    | Registro manual das ocorrências de falha e recuperação    | Interação de usuário              | Campos obrigatórios: descrição, data e hora  | Campos em branco                    | PP: Bloqueia envio se descrição estiver vazia | RA: Permite editar e reenviar                                |
| **Atualização do painel** | Sistema    | Atualização automática de dados em tempo real             | Comportamento do sistema          | Necessita conexão estável                    | Atualiza a cada 30 segundos         | PP: Exibe alerta de desconexão                | RA: Retoma sincronização automática                          |
