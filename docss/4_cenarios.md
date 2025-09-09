# Cenário de Análise/Problema

> **_NOTE:_**: A equipe deve pensar em cenários existentes na atualidade (que causam problemas para os usuários) e que a interface prevista ajudará a resolver o problema. Cenário de Análise/Problema é uma história triste. Não descreve a solução. Descreve somente o problema.

1. Cenário de Análise/Problema
2. Questões de Refinamento
3. Refinamento do Cenário Análise/Problema


---

## Jornada do usuário

A seguir, descrevemos a narrativa típica de interação do usuário com o **Boitatá-II**.  

1. **Início da interação:**  
   - O usuário (analista ou bombeiro florestal) acessa o **painel de monitoramento** via computador ou dispositivo móvel.  
   - O sistema carrega as informações do ambiente monitorado, histórico de dados e estado atual dos sensores.  

2. **Monitoramento contínuo:**  
   - Em tempo real, o sistema coleta dados dos sensores distribuídos em campo (temperatura).  
   - O usuário acompanha no painel web mapas, gráficos e índices de risco de fogo.  
   - Caso não haja anomalias, o sistema funciona de forma transparente, mantendo apenas o acompanhamento preventivo.  

3. **Detecção de evento (alerta de foco de incêndio):**  
   - O sistema identifica um aumento brusco de temperatura.  
   - Um **alerta automático** é gerado e aparece no painel do usuário, acompanhado de notificação sonora ou push.  
   - O alerta exibe a localização geográfica, horário e intensidade do evento.  

4. **Ação do usuário:**  
   - O analista confirma a informação e encaminha o alerta para a equipe de campo (bombeiros florestais).  
   - Bombeiros em campo recebem a notificação no dispositivo móvel.  
   - Dependendo da gravidade, a equipe se desloca até o local para verificar ou combater o foco de incêndio.  

5. **Encerramento da tarefa:**  
   - O alerta é armazenado no **histórico de eventos** para futuras análises.  
   - O sistema retorna ao monitoramento contínuo, aguardando novos eventos.  
