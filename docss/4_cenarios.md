<!-- # Cenário de Análise/Problema

> **_NOTE:_**: A equipe deve pensar em cenários existentes na atualidade (que causam problemas para os usuários) e que a interface prevista ajudará a resolver o problema. Cenário de Análise/Problema é uma história triste. Não descreve a solução. Descreve somente o problema.

1. Cenário de Análise/Problema
2. Questões de Refinamento
3. Refinamento do Cenário Análise/Problema


---
-->


Atores: Mariana Silva (analista de monitoramento ambiental)

**Na manhã de terça-feira** [2], **Mariana Silva**, analista de monitoramento ambiental em uma instituição pública, acessa o sistema para iniciar o cadastro e análise de ocorrências ambientais recentes [1]. Ela costuma começar seu turno **revisando os painéis com alertas de queimadas capturados por satélites e sensores distribuídos pela região sudeste do país** [5]. Os dados incluem **localização, data e hora do alerta, além de imagens térmicas** [4].

Cada foco de calor detectado precisa ser validado, registrado e encaminhado à equipe de campo, conforme o protocolo da instituição. Os dados dos alertas vêm do **sistema de sensoriamento remoto integrado ao sistema web** [3]. Durante a verificação dos registros recentes, Mariana identifica um alerta em uma área de proteção na Mata Atlântica.

Ela tenta acessar os dados meteorológicos da estação local, mas percebe que **as informações estão indisponíveis** [10]. Para seguir com a validação, Mariana entra em contato com a equipe técnica responsável pela estação **via chat interno** [13], solicitando **verificação do sensor e reenvio dos dados pelo servidor** [7]. Enquanto isso, utiliza uma fonte secundária **de imagens de satélite** para avaliar a gravidade do alerta [8].

Mariana decide continuar o processo de validação com base nos dados disponíveis e **envia uma notificação preliminar à equipe de campo, solicitando verificação do local identificado** [9]. Para garantir rastreabilidade, ela registra a ocorrência no sistema, anexando **imagens e uma descrição do problema com o sensor/servidor** [4].

No final do dia, após o restabelecimento do servidor, os dados meteorológicos são sincronizados automaticamente e Mariana valida que o alerta era real. Ela **conclui o cadastro do evento** [9], envia um e-mail para **os agentes envolvidos (campo, supervisores e analistas)** [14], e solicita confirmação das informações **por meio de um link interno do sistema** [11]. Após a confirmação, **o evento é fechado com sucesso e arquivado para o histórico de análise de risco** [12].

**Referência direta às perguntas respondidas:**
1. Quem acessa o sistema para cadastrar e analisar ocorrências ambientais?
2. Em que momento Mariana acessa o sistema para iniciar suas atividades?
3. De onde vêm os dados de alertas de queimadas?
4. Quais informações acompanham os alertas de queimadas no sistema?
5. Qual é a primeira atividade que Mariana realiza ao iniciar seu turno?
6. O que deve ser feito com cada foco de calor detectado?
7. O que Mariana solicita à equipe técnica quando identifica falha no sensor?
8. Que fonte secundária Mariana utiliza para avaliar a gravidade do alerta?
9. Que ações Mariana realiza para validar e registrar o alerta de queimada?
10. Qual dificuldade Mariana encontra ao tentar acessar os dados meteorológicos?
11. Como os agentes envolvidos confirmam as informações registradas no evento?
12. O que acontece com o evento após a confirmação das informações?
13. Como Mariana entra em contato com a equipe técnica responsável pela estação?
14. Quem recebe o e-mail enviado por Mariana após a validação do alerta?

---

Atores:  João Mendes (bombeiro florestal) 

Durante a **tarde de um sábado** [2], **João Mendes, bombeiro florestal com vasta experiência em operações diretas**, recebe um alerta em seu tablet sobre um foco de incêndio detectado próximo a uma reserva ambiental [1]. O alerta traz **dados georreferenciados da localização exata do incêndio obtidos pelo sistema de monitoramento integrado** [3]. João confere o mapa interativo em seu dispositivo móvel.

João inicia seu deslocamento imediato para o local, mantendo comunicação constante com a central **via rádio e aplicativo de mensagens** [8]. Durante o trajeto, ele recebe atualizações de novos alertas sonoros e visuais no **tablet**, que indicam mudanças no comportamento do fogo [10]. **A equipe em campo** também envia relatórios curtos sobre as condições reais encontradas, ajudando João a ajustar sua rota e estratégias [7].

Em determinado momento, João tenta acessar dados históricos da área para avaliar o risco, mas percebe que **o sistema está lento devido à baixa cobertura de rede na região** [12]. Mesmo assim, ele consegue registrar no sistema, via tablet, **as ações realizadas e a evolução do combate ao incêndio** [11].

Após cerca de duas horas de operação, o fogo é controlado com sucesso. **João envia uma última mensagem para a central** confirmando a extinção do foco [9], e **o sistema atualiza automaticamente o histórico do evento** para futuras análises [14]. Ele sente confiança no sistema que forneceu informações rápidas e precisas, permitindo uma atuação eficiente.


**Referência direta às perguntas respondidas:**
1. Quem recebe os alertas de incêndio pelo sistema de monitoramento?
2. Em que momento João recebeu o alerta do incêndio?
3. Que tipo de informação acompanha o alerta de incêndio?
4. Por qual dispositivo João acessa o mapa interativo do incêndio?
5. Como João mantém contato com a central de monitoramento durante a operação?
6. Que tipo de atualização João recebe em tempo real durante o deslocamento?
7. Quem envia relatórios das condições reais encontradas no local do incêndio?
8. Por quais meios João se comunica com a central?
9. Como João confirma a extinção do foco de incêndio?
10. Onde João acessa dados históricos para avaliar o risco da área?
11. Quais informações João registra no sistema durante a operação?
12. O que dificulta o acesso de João a dados históricos da área?
13. Quanto tempo durou a operação de combate ao fogo?
14. O que acontece no sistema após a confirmação da extinção do foco?
