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

---

## Cenário de Interação 2 – Luísa

### Resposta a Alerta e Tomada de Decisão em Campo  
**Ator:** João Pereira (técnico de campo da Defesa Civil)

João Pereira é técnico de campo responsável por verificar ocorrências de incêndio reportadas pelo sistema de monitoramento. Durante seu turno, ele recebe um alerta sonoro e visual no aplicativo do sistema, indicando um foco de calor em uma área de preservação próxima à cidade.

Ao abrir o painel, João visualiza o **mapa de sensores** com o alerta destacado em vermelho e informações sobre **temperatura, umidade e risco de propagação**. A interface do sistema permite que ele acesse rapidamente os dados detalhados do sensor que disparou o alerta.

Com base nas informações, João decide acionar a equipe de apoio, utilizando o próprio sistema para **enviar uma notificação automática** à central e **marcar o evento como “em atendimento”**. Durante o deslocamento, ele consulta as **condições meteorológicas locais** integradas ao painel para planejar a rota de acesso segura.

Chegando ao local, João confirma que o alerta é verdadeiro e atualiza o status para **“confirmado”**, adicionando fotos e observações via aplicativo.  
Após a intervenção, ele marca o evento como **“resolvido”** e registra as ações tomadas, que ficam automaticamente salvas no **histórico do sistema**.

Esse cenário evidencia como o novo sistema facilita a **tomada de decisão rápida**, melhora a **comunicação entre equipes** e reduz falhas ao integrar dados de sensores, mapas e meteorologia em uma interface única e responsiva.

**Questões de Refinamento:**

### Questões de Refinamento – Cenário 2 (João)

| Índice | Elemento     | Pergunta | Resposta |
|---------|--------------|-----------|-----------|
| [1] | **Objetivo** | Qual é o propósito principal da atividade descrita no cenário? | Garantir uma resposta rápida e eficaz a alertas de incêndio detectados pelo sistema, permitindo que o técnico de campo confirme a ocorrência, registre evidências e atualize o status em tempo real. |
| [2] | **Ambiente** | Em que contexto e local o sistema é utilizado? | O sistema é acessado por João em um dispositivo móvel durante o trabalho em campo, com acesso à rede sem fio ou conexão via dados móveis, em ambientes externos sujeitos a condições climáticas variáveis. |
| [3] | **Ator(es)** | Quem interage diretamente com o sistema? | João, técnico da Defesa Civil responsável por validar ocorrências de incêndio e coordenar as ações iniciais de resposta em campo. |
| [4] | **Planejamento** | O que o ator pretende realizar ao acessar o sistema? | João pretende verificar o alerta recebido, analisar os dados do sensor (temperatura, umidade e risco), deslocar-se até o local indicado e atualizar o status do evento conforme o andamento da operação. |
| [5] | **Ação** | Quais são as principais ações realizadas pelo ator? | Receber e abrir o alerta no aplicativo, consultar informações do sensor e mapa, acionar equipe de apoio, confirmar o evento em campo, anexar registros (fotos, observações) e finalizar o atendimento no sistema. |
| [6] | **Evento** | Que situação inesperada ou problema ocorre durante o uso? | Durante o deslocamento, João enfrenta instabilidade na conexão móvel, o que atrasa a atualização do status e dificulta o envio de evidências fotográficas no momento da confirmação do alerta. |
| [7] | **Avaliação** | Como o ator avalia o resultado de suas ações? | Após conseguir restabelecer a conexão e registrar o evento com sucesso, João avalia o sistema como prático e eficiente, destacando a utilidade do alerta automático e a integração das informações meteorológicas e geográficas. |

### Nome do Cenário: Resposta em Campo a Alertas de Incêndio

**Atores:** João Pereira (técnico da Defesa Civil)

João Pereira é técnico da Defesa Civil [3], responsável por atender a ocorrências de incêndio detectadas automaticamente pelo sistema Boitatá-II. Seu principal objetivo é garantir uma resposta rápida e eficaz aos alertas emitidos pelos sensores, validando a situação em campo e atualizando o status do evento em tempo real [1].

Durante o expediente, João acessa o sistema a partir de seu dispositivo móvel enquanto está em campo [2]. O ambiente de trabalho envolve áreas abertas e florestadas, com acesso limitado à rede móvel e exposição a condições climáticas adversas. Ele inicia o planejamento verificando os alertas ativos no aplicativo, que apresenta um mapa interativo com a localização precisa dos sensores e dados de temperatura, umidade e risco de incêndio [4].

Assim que recebe uma notificação sonora indicando um novo foco de calor, João abre o alerta e analisa as informações detalhadas do sensor, confirmando que há aumento brusco de temperatura e redução na umidade local. Ele então aciona a equipe de apoio e se desloca até o ponto indicado pelo sistema [5].

Durante o trajeto, João enfrenta instabilidade na conexão móvel, o que atrasa a sincronização dos dados e impede o envio imediato de fotos e observações do local [6]. Mesmo assim, ele registra as informações offline e, assim que o sinal é restabelecido, o sistema sincroniza automaticamente os dados com o servidor central.

Ao concluir a verificação e confirmar que se tratava de um incêndio de pequena proporção já controlado, João atualiza o status do evento para “resolvido” e anexa imagens no relatório digital. Ele avalia o sistema como prático e confiável, destacando a utilidade do alerta automático e a facilidade de uso em campo, mesmo sob condições adversas [7].

**Design Centralizado na Comunicação**

### Nome do Cenário: Resposta em Campo a Alertas de Incêndio

| Tópico > Subtópico (diálogo) | Falas e Signos |
|-------------------------------|----------------|
| **Receber alerta de foco de incêndio** | **D:** Novo alerta detectado! Sensor _#045_ indica temperatura crítica (57°C) e umidade abaixo de 20%. Deseja visualizar no mapa? <br> **U:** Sim, abrir alerta no mapa. <br> **D:** Exibindo localização do alerta: coordenadas -15.789, -47.882. Área de risco nível **alto**. |
| **Analisar dados do sensor** | **U:** Quero ver os dados detalhados do sensor. <br> **D:** Mostrando informações: temperatura atual 57°C, umidade 18%, último envio há 3 minutos. Histórico mostra aumento gradual nos últimos 15 minutos. <br> **U:** Parece um foco real, não ruído. |
| **Confirmar deslocamento para o local** | **U:** Confirmar deslocamento da equipe. <br> **D:** Confirmação registrada. GPS ativado para navegação até o ponto crítico. <br> **U:** O sistema está calculando a rota mais rápida. |
| **Registrar problema de conexão** | **U:** A conexão de dados está oscilando, o mapa parou de atualizar. <br> **D:** Conexão instável detectada. Modo offline ativado. Suas anotações e fotos serão salvas localmente até que o sinal seja restabelecido. <br> **U:** Entendido. Continuarei registrando as informações. |
| **Registrar evento e sincronizar dados** | **U:** Foco confirmado. Pequeno incêndio controlado com apoio da equipe local. <br> **D:** Deseja atualizar o status do evento para “Resolvido”? <br> **U:** Sim, e adicionar observações e fotos. <br> **D:** Dados sincronizados com sucesso. Relatório de campo atualizado no sistema central. |
| **Avaliação e encerramento** | **U:** O sistema funcionou bem, mesmo com instabilidade na rede. <br> **D:** Feedback registrado. Obrigado por contribuir com a melhoria do Boitatá-II. |


3) **Mapa de Objetivos**
> **_NOTE:_**: cada um coloca seu mapa de objetivos e deverá ter um diagrama de consolidação

4) **Esquema Conceitual de Signos**

| **Signo** | **Origem** | **Observações** | **Tipo de Conteúdo** | **Restrições sobre o Conteúdo** | **Valor Default** | **Prevenção (PP)** | **Recuperação (RA)** |
|------------|-------------|------------------|-----------------------|----------------------------------|--------------------|--------------------|----------------------|
| **Alerta de incêndio detectado** | Sistema | Notificação sonora e visual com informações do sensor e nível de risco | Comportamento do sistema | Requer sensor ativo e sincronizado com servidor | Sem alerta ativo | **PP:** Exibe aviso se dados do sensor estiverem incompletos | **RA:** Reenvia notificação caso a entrega falhe |
| **Mapa interativo de campo** | Sistema | Exibição da localização dos focos e rota até o ponto de risco | Comportamento do sistema | Requer conexão com GPS e rede móvel | Exibe mapa base com sensores em cinza | **PP:** Mostra alerta de “Sem sinal de GPS” | **RA:** Habilita modo offline com dados locais armazenados |
| **Modo offline** | Sistema | Ativado automaticamente quando a conexão móvel é perdida | Estado do sistema | Ativo apenas durante perda de conexão | Desativado | **PP:** Informa ao usuário que o modo offline foi habilitado | **RA:** Sincroniza dados automaticamente ao reconectar |
| **Registro de evento em campo** | Usuário | Formulário para descrever situação e anexar fotos | Interação de usuário (formulário) | Campos obrigatórios: descrição e imagem | Campos em branco | **PP:** Bloqueia envio sem descrição ou foto | **RA:** Permite edição e reenvio após reconexão |
| **Atualização de status do evento** | Usuário | Mudança do status (em análise / atendido / resolvido) | Interação de usuário | Requer autenticação e conexão ativa | Status: “Em análise” | **PP:** Solicita confirmação antes de alterar status | **RA:** Mantém status anterior até confirmação do servidor |
| **Sincronização automática de dados** | Sistema | Envio dos registros armazenados offline para o servidor central | Comportamento do sistema | Requer reconexão com servidor | Inativo (aguardando rede) | **PP:** Verifica integridade dos dados antes do envio | **RA:** Reenvia pacotes pendentes caso a sincronização falhe |



---


## Cenário de Interação 3 – Nathan

### Análise de Ocorrências e Geração de Relatórios  
**Atora:** Carla Mendes (coordenadora regional de monitoramento ambiental)

Carla Mendes é coordenadora responsável por acompanhar os registros de ocorrências em toda a região norte do país. Seu principal desafio é **consolidar informações de múltiplas fontes** e gerar relatórios semanais sobre os focos de incêndio detectados e atendidos.

Ao acessar o sistema, Carla utiliza o **painel de histórico** para visualizar todos os eventos registrados. Ela aplica filtros por **data, localização e status** para identificar quais alertas foram resolvidos, quais ainda estão em análise e quais demandam acompanhamento adicional.

O sistema oferece uma visão gráfica dos **indicadores de desempenho**, como tempo médio de resposta e frequência de alertas por área. A partir desses dados, Carla gera um **relatório automático em PDF**, que inclui mapas, gráficos e observações dos técnicos.

Durante a análise, Carla percebe que alguns sensores têm registros inconsistentes e usa o sistema para **enviar uma solicitação de verificação técnica**. Ela também adiciona comentários e recomendações diretamente no painel, que ficam acessíveis para toda a equipe.

O cenário destaca o papel do sistema na **gestão estratégica e documental** do processo, permitindo uma visão completa do desempenho operacional e auxiliando na **tomada de decisão baseada em dados**.  
Dessa forma, Carla consegue **reduzir retrabalhos**, **aumentar a confiabilidade das informações** e **otimizar a comunicação entre setores**.

**Questões de Refinamento**

### Questões de Refinamento – Cenário 3 (Carla)

| Índice | Elemento | Pergunta | Resposta |
|---------|-----------|-----------|-----------|
| [1] | **Objetivo** | Qual é o propósito principal da atividade descrita no cenário? | Consolidar, revisar e documentar os dados coletados pelos sensores e equipes de campo, gerando relatórios analíticos sobre ocorrências de incêndio e desempenho dos sensores. |
| [2] | **Ambiente** | Em que contexto e local o sistema é utilizado? | O sistema é acessado por Carla em seu computador de mesa no escritório da central de monitoramento ambiental, conectado à rede interna e ao banco de dados do Boitatá-II. |
| [3] | **Ator(es)** | Quem interage diretamente com o sistema? | Carla, analista técnica do órgão de monitoramento ambiental, responsável pela análise de relatórios, validação de dados e emissão de documentos oficiais de acompanhamento. |
| [4] | **Planejamento** | O que o ator pretende realizar ao acessar o sistema? | Carla pretende revisar os registros de eventos recentes, validar as informações de sensores e técnicos de campo, atualizar o status de relatórios e exportar os documentos finais em formato PDF. |
| [5] | **Ação** | Quais são as principais ações realizadas pelo ator? | Filtrar eventos registrados, consultar históricos de leitura, revisar observações das equipes, compilar dados estatísticos e gerar relatórios automáticos para o comitê gestor. |
| [6] | **Evento** | Que situação inesperada ou problema ocorre durante o uso? | Durante a revisão dos relatórios, Carla percebe inconsistências entre os dados enviados por sensores e os registros de campo, exigindo verificação manual e correção antes da emissão final. |
| [7] | **Avaliação** | Como o ator avalia o resultado de suas ações? | Após corrigir as inconsistências e gerar o relatório consolidado, Carla avalia o sistema como eficaz e confiável, destacando a clareza das visualizações e a integração automática das fontes de dados. |


### Nome do Cenário: Análise e Documentação de Relatórios de Incêndio

**Atores:** Carla Mendes (analista técnica de monitoramento ambiental)

Carla Mendes é uma analista técnica do centro de monitoramento ambiental [3], responsável por revisar, consolidar e documentar os dados provenientes dos sensores e das equipes de campo do sistema Boitatá-II. Seu principal objetivo é garantir a integridade das informações e gerar relatórios oficiais sobre as ocorrências de incêndio e o desempenho dos sensores distribuídos [1].

Durante o expediente, Carla acessa o sistema Boitatá-II a partir de seu computador de mesa, conectado à rede interna da central de monitoramento [2]. O ambiente é calmo e controlado, permitindo a análise detalhada dos registros. Ela inicia seu planejamento abrindo o painel de relatórios e filtrando os eventos registrados nos últimos sete dias para verificação [4].

No painel, Carla revisa os dados coletados pelos sensores de temperatura e umidade, além das observações enviadas pelos técnicos de campo. Ela cruza as informações para identificar padrões e validar a consistência entre os registros automáticos e os relatos manuais. Em seguida, compila as leituras em gráficos comparativos e prepara um relatório estatístico com o total de alertas recebidos e confirmados [5].

Durante a revisão, Carla percebe uma divergência entre o valor registrado por um sensor e o relatório de campo correspondente — o sensor indicava um pico de temperatura, mas o técnico registrou “sem foco detectado” [6]. Para resolver a inconsistência, ela consulta o histórico do sensor no painel técnico e atualiza o relatório com uma observação de verificação pendente.

Após revisar todas as ocorrências, Carla finaliza o documento consolidado e gera o **Relatório Semanal de Incidentes Ambientais** em formato PDF. O sistema exibe um resumo das métricas e confirma a exportação do arquivo com sucesso. Satisfeita com o resultado, Carla avalia o sistema como eficiente, claro e confiável, destacando que a integração automática entre sensores, relatórios e painéis gráficos facilita significativamente o processo de validação e comunicação institucional [7].

2) **Design Centrado na Comunicação**

### Nome do Cenário: Análise e Documentação de Relatórios de Incêndio

| **Tópico > Subtópico (diálogo)** | **Falas e Signos** |
|----------------------------------|--------------------|
| **Acessar painel de relatórios** | **U:** Preciso revisar os relatórios de eventos desta semana.<br>**D:** Acesso concedido. Painel de relatórios carregado com filtros de data e status disponíveis.<br>**U:** Vou selecionar o período dos últimos sete dias.<br>**D:** Exibindo 18 registros de eventos entre 01/11 e 07/11. |
| **Filtrar e visualizar eventos** | **U:** Quero ver apenas os eventos confirmados e pendentes de validação.<br>**D:** Filtros aplicados. Mostrando eventos classificados como “Confirmado” e “Em análise”.<br>**U:** Clico no evento “Região Serrana – Sensor_078”.<br>**D:** Exibindo detalhes: pico de temperatura 61°C, status do sensor ativo, observação de campo pendente. |
| **Verificar inconsistências de dados** | **U:** Há divergência entre o valor do sensor e o registro do técnico de campo.<br>**D:** Inconsistência detectada. Deseja marcar como “Verificação pendente”?<br>**U:** Sim, registrar observação para revisão posterior.<br>**D:** Observação adicionada ao relatório com data e hora da atualização. |
| **Gerar relatório consolidado** | **U:** Agora quero compilar os dados e gerar o relatório semanal consolidado.<br>**D:** Processando informações... 18 eventos integrados com sucesso.<br>**U:** Exportar para PDF e salvar cópia na pasta compartilhada.<br>**D:** Relatório exportado com sucesso. Arquivo salvo em `/relatorios/semana45.pdf`. |
| **Registrar encerramento da análise** | **U:** Todos os relatórios foram revisados e finalizados.<br>**D:** Status geral atualizado para “Revisão concluída”. Deseja enviar notificação ao comitê gestor?<br>**U:** Sim, enviar notificação automática.<br>**D:** Notificação enviada. Registro arquivado com sucesso. |
| **Avaliação final da usuária** | **U:** O sistema é bem intuitivo e agiliza o processo de validação dos dados.<br>**D:** Feedback registrado. Obrigado por utilizar o Boitatá-II. Sua análise foi salva no histórico de auditoria. |



3) **Mapa de Objetivos**
> **_NOTE:_**: cada um coloca seu mapa de objetivos e deverá ter um diagrama de consolidação

4) **Esquema Conceitual de Signos**

### Esquema Conceitual de Signos – Cenário 3 (Carla)

| **Signo** | **Origem** | **Observações** | **Tipo de Conteúdo** | **Restrições sobre o Conteúdo** | **Valor Default** | **Prevenção (PP)** | **Recuperação (RA)** |
|------------|-------------|-----------------|----------------------|----------------------------------|-------------------|--------------------|----------------------|
| Login no sistema | Sistema | Tela inicial de autenticação da usuária Carla | Interação de usuário (formulário) | Requer nome de usuário e senha válidos | Campos vazios | **PP:** Bloqueia acesso se credenciais inválidas | **RA:** Exibe mensagem de erro e permite nova tentativa |
| Painel de relatórios | Sistema | Interface principal para consulta de registros de eventos | Comportamento do sistema | Requer conexão com banco de dados ativo | Exibe relatórios padrão da última semana | **PP:** Alerta se o servidor estiver indisponível | **RA:** Tenta reconectar e recarregar os relatórios |
| Filtro de eventos | Usuário | Seleção de critérios de busca (data, status, sensor) | Interação de usuário | Campos obrigatórios: data inicial e final | Últimos 7 dias | **PP:** Bloqueia busca sem data definida | **RA:** Retorna ao filtro padrão e notifica o usuário |
| Detalhes do evento | Sistema | Exibição de dados técnicos e observações de campo | Comportamento do sistema | Requer registro completo no banco | Exibe status “Em análise” | **PP:** Verifica integridade dos dados antes da exibição | **RA:** Informa erro e permite recarregar informações |
| Observação de inconsistência | Usuário | Registro manual de divergência entre sensor e relatório de campo | Interação de usuário | Campos obrigatórios: descrição e data | Campo vazio | **PP:** Bloqueia envio se descrição estiver vazia | **RA:** Permite edição e reenvio da observação |
| Relatório consolidado | Sistema | Documento gerado automaticamente com base nos eventos filtrados | Comportamento do sistema | Requer todos os eventos validados | Arquivo em formato PDF | **PP:** Impede geração se houver eventos pendentes | **RA:** Exibe mensagem de pendência e sugere correção |
| Envio de notificação | Sistema | Comunicação automática ao comitê gestor após finalização | Comportamento do sistema | Requer conexão ativa e e-mails cadastrados | Mensagem padrão de conclusão | **PP:** Verifica disponibilidade de rede | **RA:** Armazena notificação em fila para reenvio |
| Feedback do usuário | Usuário | Registro opcional de avaliação sobre o sistema | Interação de usuário | Campo de texto livre | Valor nulo | **PP:** Exibe lembrete opcional para feedback | **RA:** Permite envio posterior pelo histórico |
