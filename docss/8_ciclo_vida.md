**CICLO DE VIDA DE ENGENHARIA DE USABILIDADE**

![Ciclo de vida](imagens/ciclo_de_vida.png)

1. **Características da Plataforma**  
   

| Característica | Descrição |
| :---- | :---- |
| Descrição do Software | Para o desenvolvimento da interface do projeto, foi utilizada a plataforma Grafana para melhor visualização do mapa de calor e melhor organização entre os componentes da interface como as métricas de temperatura dos sensores ativos, umidade, e riscos de fogo, fora os alertas e gráficos de relações entre região x temperatura.|
| Descrição do Hardware | Foram utilizados dois sensores de temperatura do tipo dst11 juntamente com arduínos UNO e módulos ESP32 |
| LISTA DE Capacidades da Plataforma (com explicação) | - Cadastro e login dos usuários na plataforma: usuários novos podem criar uma conta nova e tenham acesso ao sistema de monitoramento via login. - Acesso ao mapa de calor e dados de temperatura: usuários logados tem acesso ao dashboard do sistema, permitindo a visualização do mapa do Brasil e da temperatura relativa na região que se encontram os sensores, juntamente com índices de risco de incêncdio em cada área e gráficos de relação entre região x temperatura. - Sistema de alertas/notificações: o usuário cadastrado tem acesso ao painel de alertas/notificações que são atualizados em tempo real conforme mudanças de temperatura na região sendo monitorada. - Interface Web responsiva: interface com acesso via navegador com mapas interativos e gráficos personalizáveis. |
| LISTA DE Restrições da Plataforma (com explicação) | - Conexão com a internet: o sistema, sendo acessível via interface web, requer que o usuário esteja conectado à internet a todo momento, deixando o sistema propenço a riscos de baixa performance em casos de instabilidade ou qualidade baixa de conexão. - Região sendo monitorada: o sistema de monitoramento é capaz de monitorar com eficácia apenas as regiões que estão dentro da área dos sensores, podendo simular dados aproximados sobre as demais áreas por meio de dados de satélite obtidos via API. - Sensores terrestres: os sensores utilizados no projeto necessitam estar enterrados no solo da área a ser monitorada, podendo ter interferências naturais pela fauna/flora da região, ou serem de difícil acesso para manutenção. |

2. **Princípios Gerais do Projeto (INCREMENTAR TABELA)**     

| Nome | Descrição | Link |
| :---- | :---- | :---- |
| Descrição do Contexto | .  |  |
| Lei Geral de Proteção de Dados (LGPD) \- Lei n.º 13.709/2018 | A LGPD é a legislação brasileira que regulamenta o tratamento de dados pessoais no Brasil. É importante para o projeto porque estabelece regras sobre como os dados dos usuários devem ser coletados, armazenados, processados e protegidos, garantindo sua privacidade e segurança. | [https://www.planalto.gov.br/ccivil\_03/\_ato2015-2018/2018/lei/l13709.htm](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) |
| Lei n.º 10.098/2000 \- Lei da Acessibilidade |  Esta lei brasileira estabelece normas gerais e critérios básicos para a promoção da acessibilidade das pessoas com deficiência ou com mobilidade reduzida. É importante para o projeto porque define diretrizes para tornar produtos e serviços, incluindo interfaces de usuário, acessíveis a todos os usuários, independentemente de suas habilidades físicas ou cognitivas. | [https://www.planalto.gov.br/ccivil\_03/leis/l10098.htm](https://www.planalto.gov.br/ccivil_03/leis/l10098.htm) |
| ABNT NBR ISO 9241 Ergonomia da interação humano-sistema |  Esta série de normas brasileiras, baseadas nas normas ISO 9241, fornece diretrizes e orientações para o design centrado no usuário de sistemas interativos, incluindo a concepção de interfaces de usuário. A parte 210 aborda o processo de design centrado no humano, enquanto a parte 11 fornece orientações específicas sobre usabilidade. Essas normas são importantes para o projeto porque estabelecem princípios e métodos para garantir que a interface do usuário atenda às necessidades e expectativas dos usuários. | [https://www.inf.ufsc.br/\~edla.ramos/ine5624/\_Walter/Normas/Parte%2011/iso9241-11F2.pdf](https://www.inf.ufsc.br/~edla.ramos/ine5624/_Walter/Normas/Parte%2011/iso9241-11F2.pdf) |
|  | . |  |

   

3. **Metas de Usabilidade**

   1. **Qualitativo**

    


   2. **Quantitativo**  
    
| Metas | Porcentagem | Justificativa |
| ----- | :---- | :---- |
| Facilidade de … |  |  |
|  |  |  |
|  |  |  |
|  | 1% |  |
|  | 20% |  |
| **Total** | **100%** |  |
