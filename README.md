# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **Projeto Boitatá II: Monitoramento de Queimadas** sob orientação do Professor **Marco Antônio Assis De Melo** e desenvolvido pelos seguintes alunos:

- Ana Beatriz de Souza
- Luísa Graça
- Nathan Dantas

## Resumo

O Projeto Boitatá-II é um sistema de monitoramento de queimadas que utiliza tecnologia LoRa P2P para comunicação sem fio ponto a ponto. Ele permite a detecção rápida de focos de queimadas em áreas remotas com vegetação densa, oferecendo um painel de monitoramento acessível e ágil para os responsáveis pelo combate a incêndios. O sistema amplia a proposta do Boitatá-I, superando limitações de sistemas baseados em imagens de satélite, como atrasos temporais e interferência por cobertura de nuvens.

## Introdução

**Propósito e benefícios:**
O Boitatá-II visa fornecer um sistema eficiente e confiável para detecção precoce de queimadas, permitindo maior agilidade nas ações de combate e mitigação dos impactos ambientais. Seus principais benefícios incluem: detecção rápida, monitoramento em tempo real, acessibilidade em áreas remotas, e redução da dependência de sistemas convencionais de monitoramento por satélite.

**Problemas ou necessidades atendidas:**
O projeto resolve o problema da detecção tardia de queimadas em áreas remotas, que atualmente depende de imagens de satélite, muitas vezes atrasadas ou afetadas por nuvens. Também reduz a necessidade de patrulhamento manual contínuo, economizando recursos e aumentando a segurança de profissionais no campo.

**Características e funcionalidades detalhadas:**
Estações de monitoramento automáticas baseadas em Arduino;
Comunicação LoRa P2P para transmissão de dados em áreas de difícil acesso;
Painel de monitoramento central com visualização em tempo real de alertas;
Alertas automáticos de focos de queimadas via aplicativo ou painel web;
Registro histórico de eventos para análise posterior;

**Tecnologias e ferramentas:**
Hardware: Arduino, sensores de temperatura e fumaça, módulos LoRa.

Software: Painel web (HTML, CSS, JavaScript), backend em Python ou Node.js.

Comunicação: LoRa P2P, banco de dados em nuvem (ex.: MongoDB).

**Contexto de uso:**
Usuários: equipes de prevenção e combate a incêndios florestais, órgãos ambientais, pesquisadores.

Tarefas: monitoramento de áreas florestais, análise de alertas, tomada de decisões rápidas.

Equipamentos: sensores e estações LoRa, computadores ou dispositivos móveis para acessar o painel, conexão à internet ou rede LoRa.

Ambiente: áreas remotas com vegetação densa, florestas e reservas naturais.

## Publico Alvo

Grupo específico: INPE (Instituto Nacional de Pesquisas Espaciais).

**Características do público-alvo:**
Demográficas: profissionais de médio a alto nível educacional em áreas ambientais ou tecnológicas.

Comportamentais: uso frequente de tecnologia para monitoramento e gestão de riscos ambientais.

Psicográficas: preocupação com preservação ambiental, segurança e eficiência operacional.

Geográficas: regiões com risco de queimadas ou áreas de vegetação extensa, principalmente remotas ou de difícil acesso.

## Análise de concorrência

**Principais concorrentes ou softwares:**
Sistemas baseados em satélite, como o Queimadas INPE.

Sensores IoT comerciais de monitoramento ambiental.

Aplicativos de alerta ambiental (ex.: FireWatch).

**Informações coletadas:**
Sistemas de satélite têm alta cobertura, mas apresentam atrasos.

Sensores IoT comerciais geralmente têm custo elevado e alcance limitado.

**Características e funcionalidades dos concorrentes:**
Monitoramento remoto via satélite.

Alertas automatizados, mas com menor frequência.

Integração limitada com painéis interativos em tempo real.

**Experiência do usuário (UX):**
Sistemas de satélite: interface complexa e pouco amigável para usuários não técnicos.

Sensores comerciais: interfaces variáveis, geralmente pouco personalizáveis.

**Preços e modelos de negócio:**
Satélite/softwares comerciais: assinatura anual ou serviços pagos por uso.

Sensores IoT: custo inicial elevado, manutenção periódica necessária.

**Satisfação do cliente e opiniões:**
Usuários valorizam confiabilidade e precisão, mas reclamam de atrasos e custos elevados.

**Padrões e tendências:**
Crescente interesse em soluções IoT de baixo custo e longa distância de comunicação.

Necessidade de integração com alertas em tempo real e painéis centralizados.

**Relatórios e resumo dos resultados:**
Sistemas atuais apresentam limitações de custo, alcance e tempo de resposta.

Existe oportunidade para soluções que combinem baixo custo, P2P e monitoramento rápido.

**Pontos positivos e recomendações:**

Concorrentes fornecem dados confiáveis e cobertura ampla (satélite).

Recomenda-se diferenciar o Boitatá-II pela rapidez de detecção, baixo custo e acessibilidade em áreas remotas.

### Personas

- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais caracteristicas e contextos sociais, econômicos e culturais.
- Quais informações sobre o usuário o serviço ou poduto deve guardar?

  - Persona primaira ...
  - Persona secundária ...
  - Outras personas ...

### Mapa de empatia

![Mapa de empatia](empatia.png)

- Determine o mapa de empatia[^1] de pelo menos uma persona primária e uma sercundária.
  - O que o usuário vê: aqui estamos falando do ambiente visual em que o usuário se encontra. Ou seja, o que ele efetivamente enxerga, as pessoas e objetos que estão ao seu redor. Isso ajuda a entender o contexto em que o usuário está inserido e as influências visuais que está recebendo.
  - O que o usuário ouve: neste quadrante, buscamos entender o que o usuário está ouvindo, os sons que o cercam e como eles influenciam suas ações.
  - O que o usuário diz e faz: aqui consideramos ações e comportamentos que o usuário apresenta durante sua interação com serviço ou poduto.
  - O que o usuário pensa e sente: neste quadrante, buscamos entender os pensamentos, sentimentos, emoções e percepções que o usuário tem em relação ao serviço ou poduto. Quais expectativas o usuário cria sobre o serviço ou poduto?
  Que tipo de serviço ou poduto mais agrada essa persona?
  - Dores: quando falamos sobre dores do usuário, estamos fazendo referência a quaisquer obstáculos, necessidades ou frustrações que o usuário possa experimentar ao tentar realizar uma tarefa ou alcançar um objetivo. Isso inclui, por exemplo, problemas de usabilidade, dificuldades de acesso ou outros desafios que podem afetar a experiência do usuário.
  - Ganhos: nesse caso estamos falando de quaisquer benefícios ou recompensas que o usuário possa experimentar ao utilizar o serviço ou poduto. Isso pode incluir economia de tempo ou facilidade de uso, por exemplo. Que desejos do usuário o serviço ou poduto satisfaz?

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
