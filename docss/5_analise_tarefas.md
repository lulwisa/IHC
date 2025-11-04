# Análise de Tarefas
<!--
> **_NOTE:_**: A equipe deve descrever as funcionalidades mais importantes da interface/produto. A equipe deve modelar pelo menos 1 HTA, 1 GOMS e 1 CTT (de pelo menos 4 funcionalidades diferentes). Cada diagrama deve ter um texto explicando a funcionalidade.
-->
1. HTA
2. GOMS
3. CTT

---


O sistema possui as seguintes funcionalidades principais:  
1. Monitoramento em tempo real de sensores (temperatura, fumaça, umidade)  
2. Visualização de alertas em painel web  
3. Notificação de focos de queimadas para equipes de campo  
4. Registro histórico de eventos e relatórios  

---

## 1. HTA (Hierarchical Task Analysis)

**Objetivo:** Monitorar focos de incêndio e notificar equipes.  

**Tarefas hierárquicas:**
<!--
- 1. Monitorar área de risco  
  - 1.1. Inicializar painel web  
    - 1.1.1. Login no sistema  
    - 1.1.2. Carregar mapas e dados de sensores  
  - 1.2. Observar indicadores de risco em tempo real  
    - 1.2.1. Visualizar mapa de sensores  
    - 1.2.2. Conferir alertas automáticos  
- 2. Responder a alerta de foco de incêndio  
  - 2.1. Receber notificação de alerta  
  - 2.2. Confirmar dados do sensor e localização  
  - 2.3. Encaminhar alerta para equipe de campo  
- 3. Registrar ações e relatórios  
  - 3.1. Atualizar status do evento  
  - 3.2. Salvar no histórico  
  - 3.3. Gerar relatório final  
-->

| Objetivos e Operações | Problemas e Recomendações |
| :---- | :---- |
|  |  |
||  |
|  |  |
|  |   |
|  |  |

1. Acessar sistema (pré-requisito para todas as tarefas)
   - 1.1. Fazer login no sistema
   - 1.2. Carregar dashboard principal

2. Monitorar área de risco (tarefa contínua)
   - 2.1. Visualizar mapa de sensores
   - 2.2. Monitorar painel de alertas
   - 2.3. Verificar leituras individuais de sensores
       - 2.3.1. Verificar temperatura
       - 2.3.2. Verificar riscos
       - 2.3.3. Verificar umidade

3. Responder a alerta de foco de incêndio (quando foco é detectado)
   - 3.1. Receber notificação visual/sonora
   - 3.2. Analisar dados do alerta
       - 3.2.1. Verificar valores dos sensores
       - 3.2.2. Confirmar localização no mapa
       - 3.2.3. Avaliar nível de severidade
   - 3.3. Decidir ação
       - 3.3.1. Se alerta válido: encaminhar para equipe
       - 3.3.2. Se falso alarme: descartar e registrar

4. Registrar e documentar
   - 4.1. Atualizar status do evento
       - 4.1.1. Marcar status (em análise/atendimento/resolvido)
       - 4.1.2. Inserir observações
   - 4.2. Salvar no histórico
   - 4.3. Gerar relatório
       - 4.3.1. Exportar arquivo

<!-- **Explicação:**  
O HTA mostra a sequência hierárquica de tarefas, desde o monitoramento em tempo real até a tomada de decisão e registro do evento, detalhando sub-tarefas que os usuários realizam no painel e em campo.  

---
-->

---

## 2. GOMS (Goals, Operators, Methods, Selection rules)

<!-- **Funcionalidade:** Notificação de focos de queimadas para equipes de campo  

- **Goal (Objetivo):** Notificar rapidamente a equipe sobre um foco de incêndio detectado.  
- **Operators (Operadores):**  
  - Clicar em botão do painel  
  - Digitar informações de localização  
  - Selecionar equipe responsável  
  - Confirmar envio do alerta  
- **Methods (Métodos):**  
  1. Sistema detecta aumento de temperatura/fumaça → gera alerta automático  
  2. Usuário recebe alerta no painel → verifica localização e intensidade  
  3. Usuário seleciona a equipe de campo → envia notificação via aplicativo ou e-mail  
- **Selection Rules (Regras de Seleção):**  
  - Se intensidade do fogo > limite crítico → enviar alerta prioritário  
  - Se sensor offline → notificar equipe de manutenção antes de enviar alerta  

**Explicação:**  
O GOMS detalha como o usuário interage com o painel para notificar focos de queimadas, listando ações, métodos e regras que guiam a tomada de decisão.  

---

-->

## Análise GOMS - Sistema de Monitoramento de Incêndios

GOAL 0: Monitorar focos de incêndio e notificar equipes

- GOAL 1: Acessar o sistema de monitoramento
  - METHOD 1.1: Login no sistema
  - SEL.RULE: os campos obrigatórios devem ser preenchidos (email e senha)

    - OP 1.1.1: Localizar campo de usuário
    - OP 1.1.2: Digitar email do usuário
    - OP 1.1.3: Localizar campo de senha
    - OP 1.1.4: Digitar senha
    - OP 1.1.5: Clicar no botão "Entrar"
    - OP 1.1.6: Aguardar carregamento da dashboard
    - OP 1.1.7: Verificar se dashboard foi carregada corretamente


- GOAL 2: Monitorar área de risco continuamente  
  - METHOD 2.1: Visualizar mapa de sensores
  - SEL.RULE: Se a temperatura do sensor estiver elevada (indicando risco de fogo), o sensor deve se destacar visualmente com a cor vermelha.

    - OP 2.1.1: Localizar área do mapa no dashboard
    - OP 2.1.2: Observar indicadores visuais dos sensores
    - OP 2.1.3: Identificar cores e ícones de status (temperatura normal, elevada, crítica)

  - METHOD 2.2: Monitorar painel de alertas
  - SEL.RULE: O painel de notificações deve ser visível em uma seção fixa da tela durante o monitoramento.

    - OP 2.2.1: Localizar painel de notificações
    - OP 2.2.2: Verificar presença de novos alertas
    - OP 2.2.3: Ler mensagens de alerta

  - METHOD 2.3: Verificar leituras de sensores individuais
  - SEL.RULE: Se o usuário selecionar um sensor, ele deve visualizar informações detalhadas sobre o sensor selecionado, com dados atualizados em tempo real (como temperatura e umidade).
    
    - OP 2.3.1: Selecionar sensor no mapa
    - OP 2.3.2: Ler valor de temperatura exibido
    - OP 2.3.3: Ler valor de umidade
    - OP 2.3.4: Comparar valores com limites normais
    - OP 2.3.5: Fechar janela de detalhes do sensor

- GOAL 3: Responder a alerta de foco de incêndio
  - METHOD 3.1: Identificar e analisar alerta
  - SEL.RULE: O alerta visual deve ser destacado com uma cor forte (vermelho) se o nível de risco de fogo for crítico.

    - OP 3.1.1: Perceber notificação visual
    - OP 3.1.2: Clicar no alerta para abrir detalhes
    - OP 3.1.3: Ler informações do sensor acionado
    - OP 3.1.4: Localizar ponto no mapa
    - OP 3.1.5: Verificar timestamp do alerta
    - OP 3.1.6: Ler nível de severidade (baixo, médio, alto)

  - METHOD 3.2: Validar alerta
  - SEL.RULE: O sistema deve comparar os dados atuais com o histórico do sensor para determinar se há uma mudança significativa e indicar qualquer anomalia (ex: valor de temperatura muito superior ao histórico recente).

    - OP 3.2.1: Comparar dados atuais com histórico
    - OP 3.2.2: Verificar demais sensores 
    - OP 3.2.3: Avaliar padrão de leituras
    - OP 3.2.4: Tomar decisão (válido ou falso positivo)

  - METHOD 3.3a: Encaminhar alerta válido
  - SEL.RULE: O botão "Encaminhar" deve estar desabilitado até que todos os campos obrigatórios (email da equipe, mensagem de alerta) sejam preenchidos.

    - OP 3.3a.1: Clicar em botão "Encaminhar"
    - OP 3.3a.2: Selecionar email da equipe de campo
    - OP 3.3a.3: Confirmar envio
    - OP 3.3a.4: Verificar confirmação de notificação enviada

  - METHOD 3.3b: Descartar falso alarme
  - SEL.RULE: Após o descarte, o alerta deve ser removido da lista de notificações.
  
    - OP 3.3b.1: Clicar em botão "Descartar alerta"
    - OP 3.3b.2: Confirmar descarte

- GOAL 4: Registrar e documentar eventos
  - METHOD 4.1: Atualizar status do evento
  - SEL.RULE: O sistema deve validar que um novo status foi selecionado corretamente (ex: "Em andamento", "Em análise", etc.).

    - OP 4.1.1: Localizar evento na dashboard
    - OP 4.1.2: Clicar no evento para abrir detalhes
    - OP 4.1.3: Clicar em campo "Status"
    - OP 4.1.4: Selecionar novo status (Em análise/Em andamento/Resolvido)
    - OP 4.1.5: Clicar em "Salvar"
    - OP 4.1.6: Verificar atualização confirmada

  - METHOD 4.2: Gerar relatório
  - SEL.RULE: O botão "Gerar" deve estar desabilitado até que todas as seleções de data e formato de exportação sejam feitas.

    - OP 4.2.1: Navegar até seção "Relatórios"
    - OP 4.2.2: Clicar em "Novo Relatório"
    - OP 4.2.3: Selecionar data inicial
    - OP 4.2.4: Selecionar data final
    - OP 4.2.5: Selecionar formato de exportação (PDF/Excel)
    - OP 4.2.6: Clicar em "Gerar"
    - OP 4.2.7: Aguardar processamento
    - OP 4.2.8: Baixar arquivo gerado

---

## 3. CTT (ConcurTaskTrees)

**Funcionalidade:** Visualização de alertas e monitoramento de sensores  

(Ana)

