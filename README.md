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
- Sistemas de monitoramento baseados em satélite;  
- Sensores IoT comerciais de monitoramento ambiental;  
- Aplicativos de alerta ambiental, como o FireWatch.

**Características e funcionalidades dos concorrentes:**  
- Monitoramento remoto via satélite;  
- Alertas automatizados, mas com menor frequência;  
- Integração limitada com painéis interativos em tempo real;  
- Falhas de segurança.

**Experiência do usuário (UX):**  
- Sistemas de satélite: interface complexa e pouco amigável para usuários não técnicos;  
- Sensores comerciais: interfaces variáveis, geralmente pouco personalizáveis.

**Preços e modelos de negócio:**  
- Satélite/softwares comerciais: assinatura anual ou serviços pagos por uso;  
- Sensores IoT: custo inicial elevado, manutenção periódica necessária.

**Satisfação do cliente e opiniões:**  
- Usuários valorizam confiabilidade e precisão, mas reclamam de atrasos e custos elevados.

**Padrões e tendências:**  
- Crescente interesse em soluções IoT de baixo custo e longa distância de comunicação;  
- Necessidade de integração com alertas em tempo real e painéis centralizados.

**Relatórios e resumo dos resultados:**  
- Sistemas atuais apresentam limitações de custo, alcance e tempo de resposta;  
- Existe oportunidade para soluções que combinem baixo custo, P2P e monitoramento rápido.

**Pontos positivos e recomendações:**  
- Concorrentes fornecem dados confiáveis e cobertura ampla (satélite);  
- Recomenda-se diferenciar o **Projeto Boitatá-II** pela rapidez de detecção, baixo custo, escalabilidade e acessibilidade em áreas remotas.

#### Personas

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
- ONGs ambientais que monitoram impactos ecológicos em tempo real.  

### Mapa de empatia

![Mapa de empatia](empatia.png)

#### Persona primária: Analista de Monitoramento Ambiental

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


#### Persona secundária: Bombeiro Florestal

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
 
  
## Contexto de uso

- Descreva o ambiente em que o serviço ou poduto deve ser utilizado.
- Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
- Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
- O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?

## Jornada do usuário

- Criar uma narrativa para o o seu serviço ou poduto com o usuário.
- Determine o que o usuário realiza desde a primeira até o última interação com o serviço ou poduto.
  - Descreva o que acontece ou pode acontecer passo a passo
  - Como a tarefa começa? Como a tarefa se desenvolve? Como a tarefa termina?


<!--
## Análise de concorrência

- Pesquise serviços ou podutos existentes atualmente que possam realizar o objetivo deste projeto.
- Selecione pelo menos 3 serviços ou podutos diferentes.
- Em relação aos concorrentes, respondam as seguintes perguntas?
  - Existe plataforma similar que atende o mesmo mercado e funcionalidades? Se sim: Quais os pontos positivos? Quais os pontos negativos?
  - Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado? Se sim: Quais os pontos positivos? Quais os pontos negativos?
 -->
 
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
