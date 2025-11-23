## AVALIAÇÃO HEURÍSTICA DE NIELSEN

## Relatório de Avaliação Heurística - **Ana**

### Violações Identificadas

| Nº | Heurística | Gravidade | Observação | Print de tela |
|----|------------|-----------|------------|-------|
| 1 | **Visibilidade do status do sistema** | 2 | Ao carregar o mapa de sensores, não há indicador visual claro do progresso. O usuário fica sem saber se o sistema está realmente processando as informações. | - |
| 3 | **Controle e liberdade para o usuário** | 3 | Não existe opção de selecionar dispositivo apenas selecionando em algum na tabela, obrigando o usuário a procurar no mapa manualmente. | - |
| 6 | **Reconhecimento em lugar de lembrança** | 2 | Os ícones dos sensores no mapa não possuem legenda explícita, forçando o usuário a interagir para identificar o ID ou nome do mesmo. | - |

### Resumo da Avaliação
**Total de problemas:** 3  
**Gravidade média:** 2 <br>
**Prioridade:** MÉDIA

### Recomendações
1. Implementar spinner de carregamento durante requisições
3. Adicionar seleção de dispositivos dinâmica para melhorar a experiência do usuário
6. Incluir legenda interativa para maior clareza nos ícones do mapa

---

## Relatório de Avaliação Heurística - **Luisa**

### Violações Identificadas

| Nº | Heurística | Gravidade | Observação | Print de tela |
|----|------------|-----------|------------|-------|
| 2 | **Compatibilidade sistema/mundo real** | 2 | Termos técnicos são usados em mensagens para o usuário final, o que pode causar confusão aos usuários não familiarizados com o desenvolvimento de software. | - |
| 4 | **Consistência e padrões** | 3 | As funcionalidades do painel trabalham de maneira individual, o que pode dificultar a visualização da correlação das informações de um mesmo dispositivo (Ex: Alerta de temperatura de um dispositivo e localização do mesmo no mapa). | - |
| 8 | **Projeto minimalista** | 1 | A tela principal apresenta muitas métricas secundárias que competem pela atenção com os dados críticos de alertas. | - |
| 9 | **Recuperação de erros** | 4 | Quando ocorre falha de conexão, a mensagem exibe código de erro técnico sem explicação em linguagem natural ou sugestão de solução. | - |

### Resumo da Avaliação
**Total de problemas:** 4  
**Gravidade média:** 3 <br>
**Prioridade:** ALTA

### Recomendações
2. Traduzir termos técnicos para linguagem simplificada a qualquer usuário
4. Padronizar correlação das janelas em relação ao mesmo dispositivo
8. Criar hierarquia/prioridade visual para informações críticas vs secundárias
9. Melhorar mensagens de erro com linguagem clara e possíveis soluções

---

## Relatório de Avaliação Heurística - **Nathan**

### Violações Identificadas

| Nº | Heurística | Gravidade | Observação | Print de tela |
|----|------------|-----------|------------|-------|
| 5 | **Prevenção de erros** | 3 | O sistema demonstra erros técnicos no histórico de temperatura caso não tenha nenhuma temperatura medida nas últimas horas, resultando em um erro que poderia ser prevenido com validação prévia. | - |
| 7 | **Flexibilidade e eficiência** | 2 | Usuários avançados não possuem atalhos de teclado ou opções de lote para operações repetitivas como deletar múltiplos dispositivos de uma vez. | - |
| 10 | **Ajuda e documentação** | 4 | Não existe seção de ajuda integrada, tutorial ou documentação acessível dentro do sistema para orientar novos usuários, o que leva o usuário a ler documentações no GitHub ou fontes alternativas sobre as funcionalidades. | - |

### Resumo da Avaliação
**Total de problemas:** 3  
**Gravidade média:** 3 <br>
**Prioridade:** ALTA

### Recomendações
5. Implementar validações em tempo real no painel
7. Adicionar atalhos (teclado/mouse) e operações em larga escala (Ex: Múltipla seleção)
10. Desenvolver sistema de ajuda contextual e tutorial integrado

---

### LEGENDA DE GRAVIDADE

| Grau | Tipo | Descrição |
|------|------|-----------|
| 0 | Sem importância | Não afeta a operação |
| 1 | Cosmético | Melhoria visual, sem urgência |
| 2 | Simples | Problema de baixa prioridade |
| 3 | Grave | Deve ser reparado com prioridade |
| 4 | Catastrófico | Bloqueia funcionalidades críticas |
