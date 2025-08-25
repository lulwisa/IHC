# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **Projeto Boitatá II: Monitoramento de Queimadas** sob orientação do Professor **Marco Antônio Assis De Melo** e desenvolvido pelos seguintes alunos:

- Ana Beatriz de Souza
- Luísa Graça
- Nathan Dantas

## Resumo

O **Projeto Boitatá-II** é um sistema de monitoramento de queimadas que utiliza tecnologia **LoRa P2P** para comunicação sem fio ponto a ponto. Ele permite a detecção rápida de focos de queimadas em áreas remotas com vegetação densa, oferecendo um painel de monitoramento acessível e ágil para os responsáveis pelo combate a incêndios. O sistema amplia a proposta do **Projeto Boitatá-I**, superando limitações de sistemas baseados em imagens de satélite, como atrasos temporais e interferência por cobertura de nuvens.

---

## Introdução

**Propósito e benefícios:**  
O Boitatá-II visa fornecer um sistema eficiente e confiável para detecção precoce de queimadas, permitindo maior agilidade nas ações de combate e mitigação dos impactos ambientais.  
Principais benefícios:  
- Detecção rápida de focos de incêndio;  
- Monitoramento em tempo real;  
- Acessibilidade em áreas remotas;  
- Redução da dependência de sistemas convencionais de satélite;  
- Inclusão do índice de **Risco de Fogo/Programa Queimadas**;  
- Baixo tempo de resposta para alertas.  

**Problemas ou necessidades atendidas:**  
O projeto resolve a detecção tardia de queimadas em áreas remotas, que atualmente depende de imagens de satélite atrasadas ou com interferência de nuvens. Também reduz a necessidade de patrulhamento manual contínuo, economizando recursos e aumentando a segurança de profissionais no campo.  

**Características e funcionalidades:**  
- Estações de monitoramento automáticas baseadas em Arduino;  
- Comunicação **LoRa P2P** para transmissão de dados em áreas de difícil acesso;  
- Painel de monitoramento central com visualização em tempo real de alertas;  
- Alertas automáticos via aplicativo ou painel web.

**Tecnologias e ferramentas:**  
- **Hardware:** Arduino MKR WAN 1310, sensor de temperatura DS18B20, antena amplificadora monopolo;  
- **Software:** máquinas virtuais (VMware Workstation + Ubuntu), painel web integrado com React.js, backend em Java (SpringBoot + Maven);  
- **Comunicação:** LoRa P2P, banco de dados PostgreSQL, CloudFlare Tunnel (Zero Trust), OpenVPN, Docker Compose.

**Contexto de uso:**  
- **Usuários:** equipes de prevenção e combate a incêndios florestais, órgãos ambientais, pesquisadores;  
- **Tarefas:** monitoramento de áreas florestais, análise de alertas, tomada de decisões rápidas;  
- **Equipamentos:** sensores e estações LoRa, computadores ou dispositivos móveis para acessar o painel, conexão à internet ou rede LoRa;  
- **Ambiente:** áreas remotas com vegetação densa, florestas e reservas naturais.

---

## Público Alvo

**Grupo específico:**  
- INPE (Instituto Nacional de Pesquisas Espaciais).

**Características do público-alvo:**  
- **Demográficas:** profissionais de médio a alto nível educacional em áreas ambientais ou tecnológicas;  
- **Comportamentais:** uso frequente de tecnologia para monitoramento e gestão de riscos ambientais;  
- **Psicográficas:** preocupação com preservação ambiental, segurança e eficiência operacional;  
- **Geográficas:** regiões com risco de queimadas ou áreas de vegetação extensa, principalmente remotas ou de difícil acesso.

---

## Análise de concorrência

**Principais concorrentes ou softwares:** 

Imagem Geosistemas — Painel de SP:

Empresa brasileira que desenvolveu um painel GIS para o Corpo de Bombeiros de São Paulo. Detecta até 14 mil focos de calor em tempo real, com atualização a cada 15 minutos, usando dados do satélite VIIRS e oferecendo visualização intuitiva para resposta rápida.

SELVA – UEA (Brasil):

Aplicativo brasileiro de baixo custo criado pela Universidade do Estado do Amazonas. Monitora queimadas em tempo real na Amazônia, além de qualidade do ar, chuvas e descargas elétricas. Usa dados de satélite e sensores terrestres, com visualização clara e filtros por satélite.

**Características e funcionalidades dos concorrentes:**

Imagem Geosistemas — Painel de SP:
- Atualização de dados em tempo real a cada 15 minutos;
- Monitoramento de até 14 mil focos de calor simultâneos;
- Uso do satélite VIIRS para coleta de dados;
- Visualização intuitiva e georreferenciada para suporte rápido à tomada de decisão.

SELVA – UEA:
- Monitoramento em tempo real de queimadas na Amazônia;
- Integração de dados de satélite com sensores terrestres;
- Monitoramento adicional da qualidade do ar, chuvas e descargas elétricas;
- Visualização clara com filtros por satélite que facilitam a análise.

**Experiência do usuário (UX):** 

Imagem Geosistemas — Painel de SP:
Interface amigável, focada em facilitar a resposta rápida por órgãos de segurança pública, com painéis gráficos que suportam decisões emergenciais.

SELVA – UEA:
Interface acessível e clara, com filtros personalizáveis que atendem diferentes perfis de usuários, desde pesquisadores até agentes de campo.

**Preços e modelos de negócio:** 

Imagem Geosistemas — Painel de SP:
Provavelmente opera com contratos governamentais, modelo de licenciamento ou prestação de serviço, sem informações públicas claras sobre preços. Usuários restritos apenas a funcionários do corpo de bombeiros.

SELVA – UEA:
Solução de baixo custo, desenvolvida por universidade pública, disponibilizada com acesso gratuito na loja de aplicativos de smartphones.

**Satisfação do cliente e opiniões:**

Imagem Geosistemas — Painel de SP:
Usuários destacam a confiabilidade e rapidez da detecção, valorizando a interface intuitiva para operações emergenciais. Algumas demandas por atualizações ainda mais frequentes.

SELVA – UEA:
Usuários apreciam o custo acessível e a abrangência do monitoramento ambiental, mas existem limitações em cobertura e suporte em áreas muito remotas.

**Padrões e tendências:**

Ambos os concorrentes seguem a tendência de combinar dados de satélites com sensores para aumentar a precisão do monitoramento ambiental.
Valorização crescente de interfaces acessíveis que atendam tanto especialistas quanto usuários de campo.
Demanda por soluções de baixo custo que possam ser escaláveis para grandes regiões, como a Amazônia.

**Relatórios e resumo dos resultados:** 

Imagem Geosistemas — Painel de SP: Sistema robusto, confiável e rápido, porém dependente de dados satelitais com atualizações a cada 15 minutos, o que pode limitar a imediaticidade em alguns casos, e restrito apenas a funcionários do corpo de bombeiros.

SELVA – UEA: Aplicativo inovador, com integração multi-sensorial e custo reduzido, porém com desafios em cobertura e suporte em regiões mais afastadas.

**Pontos positivos e recomendações:**

Imagem Geosistemas: Forte na rapidez e confiabilidade dos dados, com excelente interface para resposta emergencial; recomendável explorar atualização ainda mais frequente; acessível a todo o público.

SELVA – UEA: Diferencial no baixo custo e na abrangência ambiental (incluindo qualidade do ar e descargas elétricas); recomendável ampliar a cobertura (foco somente no estado do Amazonas) e o suporte técnico em áreas remotas maiores; incluir avisos para possíveis riscos de queimada.

Para o Projeto Boitatá-II, recomenda-se focar na combinação dos pontos fortes desses dois concorrentes: detecção rápida e confiável, baixo custo, escalabilidade para áreas remotas, interface amigável para diversos perfis de usuário e acesso livre.

---

## Personas

O Projeto Boitatá-II possui diferentes tipos de usuários, cada um com necessidades específicas em relação ao monitoramento de queimadas.  

**Persona primária: Analista de Monitoramento Ambiental**

- **Contexto social/econômico/cultural:**  
  Profissional com formação em áreas ambientais ou tecnológicas, trabalha em órgãos governamentais ou institutos de pesquisa, geralmente com experiência prévia em monitoramento ambiental e uso de tecnologias de informação. Recebe pressão por relatórios precisos e rápidos sobre focos de incêndio.  
- **Informações que o serviço deve guardar:**  
  - Histórico de alertas de queimadas por região;  
  - Dados de sensores em tempo real;  
  - Logs de intervenções e ações tomadas;  
  - Perfis de usuários e permissões de acesso.  

**Persona secundária: Bombeiro Florestal**

- **Contexto social/econômico/cultural:**  
  Profissional de campo, atuando diretamente na prevenção e combate a incêndios florestais. Experiência prática, mas nem sempre alta familiaridade com tecnologias avançadas. Valoriza informações rápidas e confiáveis para tomada de decisões em situações críticas.  
- **Informações que o serviço deve guardar:**  
  - Alertas de foco de incêndio em tempo real;  
  - Localização e status de equipamentos de combate;  
  - Histórico de ocorrências e ações realizadas;  
  - Notificações personalizadas conforme região de atuação.  

**Outras personas**

- Pesquisadores ambientais interessados em dados históricos de queimadas;  
- Gestores de unidades de conservação que precisam planejar estratégias de prevenção;  
- ONGs ambientais que monitoram impactos ecológicos em tempo real;
- Moradores de áreas de risco de queimadas.

### Mapa de empatia

![Mapa de empatia](empatia.png)

#### Persona primária: Analista de Monitoramento Ambiental
Nome: Mariana Silva

Idade: 34 anos

Cargo: Analista de Monitoramento Ambiental

Local de Trabalho: Centro de Monitoramento Ambiental de uma instituição pública

Formação: Engenharia Ambiental, com especialização em sensoriamento remoto e geotecnologias

Habilidades técnicas: Sistemas de informação geográfica (SIG), análise de dados ambientais, relatórios técnicos  

- **O que o usuário vê:**  
  - Painéis web com gráficos, mapas e alertas em tempo real;  
  - Equipe de colegas trabalhando simultaneamente;  
  - Relatórios de satélite e sensores;  
  - Notificações de focos de queimadas.  

- **O que o usuário ouve:**  
  - Comunicação interna da equipe;  
  - Alertas sonoros do sistema;  
  - Informações recebidas de outras agências ou órgãos ambientais.  

- **O que o usuário diz e faz:**  
  - Analisa dados e identifica regiões críticas;  
  - Compartilha alertas com equipes de campo;  
  - Atualiza registros e envia relatórios periódicos;  
  - Interage com o painel para filtrar e visualizar informações específicas.  

- **O que o usuário pensa e sente:**  
  - Sente responsabilidade pela precisão dos alertas;  
  - Preocupa-se com o tempo de resposta e confiabilidade do sistema;  
  - Espera um sistema ágil, intuitivo e seguro;  
  - Valoriza dados claros e fáceis de interpretar para tomada de decisão rápida.  

- **Dores:**  
  - Atraso na recepção de dados;  
  - Falta de integração com diferentes fontes de informação;  
  - Painéis complexos ou pouco intuitivos;  
  - Falta de histórico ou registro confiável de eventos.  

- **Ganhos:**  
  - Receber alertas em tempo real;  
  - Facilitar tomada de decisões com informações precisas;  
  - Acesso a histórico de dados confiável;  
  - Interface intuitiva e de fácil interpretação.


#### Persona primária: Bombeiro Florestal
Nome: João Mendes

Idade: 41 anos

Cargo: Bombeiro Florestal

Local de Atuação: Campo (operações diretas em áreas de risco ambiental)

Formação: Treinamento técnico em combate a incêndios florestais, experiência em campo

Habilidades técnicas: Uso de GPS, comunicação via rádio, leitura de mapas e atuação em áreas de risco


- **O que o usuário vê:**  
  - Área de operação com sensores distribuídos;  
  - Alertas visuais em dispositivos móveis ou tablets;  
  - Outros membros da equipe em campo.  

- **O que o usuário ouve:**  
  - Sons de alertas do sistema;  
  - Comunicações da equipe via rádio ou aplicativo;  
  - Ambiente natural (vento, animais, fogo).  

- **O que o usuário diz e faz:**  
  - Recebe alertas e se desloca para o foco de incêndio;  
  - Registra ocorrências e ações no sistema;  
  - Comunica atualizações à central e colegas de campo.  

- **O que o usuário pensa e sente:**  
  - Precisa de confiança nas informações para agir rapidamente;  
  - Sente pressão em situações de emergência;  
  - Valoriza sistemas intuitivos e confiáveis;  
  - Quer reduzir riscos pessoais e maximizar eficiência da equipe.  

- **Dores:**  
  - Alertas atrasados ou imprecisos;  
  - Falta de dados claros sobre a localização e intensidade do fogo;  
  - Dificuldade de acesso a informações no campo;  
  - Interfaces complexas ou pouco responsivas em dispositivos móveis.  

- **Ganhos:**  
  - Alertas rápidos e precisos em dispositivos móveis;  
  - Informação georreferenciada sobre focos de incêndio;  
  - Sistema confiável mesmo em áreas remotas;  
  - Redução de risco e melhoria na eficiência das operações.


#### Persona Secundária: Cidadã Engajada e Moradora de Área de Risco
Nome: Carla Torres

Idade: 29 anos

Ocupação: Professora do Ensino Fundamental

Localização: Moradora da zona rural de um município que sofre com queimadas sazonais

Formação: Licenciatura em Pedagogia

Habilidades técnicas: Uso básico de tecnologia (apps, redes sociais, mapas online)

- **O que vê:**
  - Aplicativo ou site com alertas de risco ambiental próximos
  - Mapa com focos de incêndio próximos ou históricos na região
  - Notificações simples no celular sobre qualidade do ar e situação atual
  - Dicas de prevenção e segurança

- **O que ouve:**
  - Alertas do app quando há risco nas proximidades
  - Notícias locais sobre queimadas e clima seco
  - Conversas de vizinhos e da comunidade sobre o risco de incêndios

- **O que diz e faz:**
  - Verifica o app com frequência durante a estação seca
  - Compartilha informações com vizinhos e familiares
  - Entra em contato com autoridades locais se notar algo suspeito
  - Usa as informações para se preparar ou evitar áreas de risco

- **O que pensa e sente:**
  - Preocupada com a segurança da família, principalmente durante épocas críticas
  - Deseja informações confiáveis, acessíveis e em linguagem clara
  - Quer se sentir parte da solução, mesmo sem estar diretamente envolvida no combate
  - Busca tranquilidade ao saber que está bem informada

- **Dores:**
  - Falta de acesso a informações de qualidade em tempo real
  - Termos técnicos e mapas complicados de entender
  - Notificações genéricas ou alarmistas que não ajudam na prática
  - Falta de confiança em fontes não oficiais

- **Ganhos:**
  - Receber alertas localizados e compreensíveis diretamente no celular
  - Entender com facilidade se está em área de risco ou não
  - Poder tomar decisões conscientes e rápidas (como evacuar, proteger bens, avisar vizinhos)
  
---

## Contexto de uso

- **Ambiente de utilização:**  
  O sistema deve ser utilizado em **áreas remotas com vegetação densa**, florestas, reservas ambientais e regiões de risco de queimadas. Também será usado em **centros de monitoramento** urbanos ou regionais, onde os dados coletados são analisados em tempo real.  

- **Contextos sociais, econômicos e culturais:**  
  - **Social:** prevenção e monitoramento de desastres ambientais que impactam populações locais e comunidades que dependem da floresta para subsistência;  
  - **Econômico:** redução de custos em combate a incêndios, minimização de prejuízos econômicos logísticos e causados pela destruição de áreas agrícolas e florestais;  
  - **Cultural:** preservação de biomas e territórios tradicionais, como áreas indígenas e comunidades ribeirinhas que sofrem diretamente os efeitos das queimadas.  

- **Informações do ambiente que devem ser guardadas antes da interação:**  
  - Localização geográfica e delimitação da área monitorada;  
  - Histórico de queimadas ou focos anteriores;  
  - Índices climáticos e de risco de fogo;  
  - Estado atual dos sensores e estações (ativos/inativos);  
  - Informações sobre usuários autorizados a receber notificações.  

- **O que normalmente está acontecendo no ambiente durante a interação:**  
  - Em campo: sensores estão monitorando a temperatura, coletando dados continuamente;  
  - No centro de controle: usuários analisam dados em tempo real no painel, recebem alertas de novos focos e gerenciam relatórios;  
  - Em situação de alerta: o sistema dispara notificações para bombeiros florestais ou órgãos ambientais, indicando o foco de incêndio.  

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

---


 
## Coleta de dados

## Modelo de tarefas

## Design

- Pense nas características de Affordances do seu serviço ou poduto. 
    - Que tipo de acessibilidades devem ser consideradas dentro do seu projeto?
- Discuta o papel das expectativas do usuário no projeto deste serviço ou poduto. Qual a importância e pontos a serem considerados se você quiser vender esse serviço ou poduto?

### Prototipação em baixo nível (papel)
#### Avaliação heurística

### Prtotipação em médio nível (Figma)
#### Avaliação heurística

### Prtotipação em alto nível (React)
#### Avaliação heurística

[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

<!-- TODOs:
- Add exemplos
 -->
