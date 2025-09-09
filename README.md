# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](http://lattes.cnpq.br/6747210702910392) e Prof. Dr. [Plino Thomaz Aquino Junior](http://lattes.cnpq.br/6186413528999908).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **Título do TCC** sob orientação do Professor **Nome do Orientador** e desenvolvido pelos seguintes alunos:

- Ana Beatriz de Souza
- Luísa Graça
- Nathan Dantas

## Conhecendo o problema

Sobre o produto ou serviço que seu grupo está desenvolvendo, responda:
- Apresente uma breve descrição.
- Apresente o objetivo. 
- Apresente o usuário final.
- Apresente os principais benefícios para o usuários.
- Apresente as funcionalidades.
- Apresente as tecnologias e ferramentas computacionais utilizadas.
- Apresente o contexto de uso.
- O produto ou serviço prevê o desenvolvimento de interface? (Sim/Não)

---

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

## Desenvolvimento
- [Análise de Concorência](docs/2_concorencia.md)
- [Personas](docs/3_personas.md)
- [Cenário de Análise/Problema](docs/4_cenarios.md)
- [Análide de Tarefas](docs/5_analise_tarefas.md)
- [Prototipação em Papel](docs/6_prototipacao.md)
- [Coleta de Dados](docs/7_coleta_dados.md)
- [Ciclo de vida da engenharia de usabilidade](docs/8_ciclo_vida.md)
- [Modelo Conceitual](docs/9_modelo_conceitual.md) 
- [MOLIC](docs/10_molic.md)
- [FIGMA](docs/11_figma.md)
- [Planejamento da Avaliação](docs/12_planejamento_avaliacao.md)
- [Avaliação de IHC através de Inspeção Heurística](docs/13_heuristica.md)
- [Avaliação de Usabilidade baseado em Observação do Usuário](docs/14_observacao_usuario.md)
