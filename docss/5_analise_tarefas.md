# Análise de Tarefas

> **_NOTE:_**: A equipe deve descrever as funcionalidades mais importantes da interface/produto. A equipe deve modelar pelo menos 1 HTA, 1 GOMS e 1 CTT (de pelo menos 4 funcionalidades diferentes). Cada diagrama deve ter um texto explicando a funcionalidade.

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

**Explicação:**  
O HTA mostra a sequência hierárquica de tarefas, desde o monitoramento em tempo real até a tomada de decisão e registro do evento, detalhando sub-tarefas que os usuários realizam no painel e em campo.  

---

## 2. GOMS (Goals, Operators, Methods, Selection rules)

**Funcionalidade:** Notificação de focos de queimadas para equipes de campo  

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

## 3. CTT (ConcurTaskTrees)

**Funcionalidade:** Visualização de alertas e monitoramento de sensores  
