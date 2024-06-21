[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/cQThrnt4)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15267820&assignment_repo_type=AssignmentRepo)
# INF0429 - Robotics

## Seminário

### Integrantes
202010396 - FRANCIELI MOREIRA DE CARVALHO

202005489 - JONAS GOMES DA SILVA JÚNIOR

202005498 - MATHEUS FARES COSTA BRAKES

202005506 - VICTOR GUERREIRO PIMENTA
 

# Robô Assistente para Distribuição de Medicamentos em Hospitais
**Francieli M. de Carvalho¹, Jonas G. S. Junior², Matheus F. C. Brakes³, Victor G. Pimenta⁴**

¹²³⁴Instituto de Informática – Universidade Federal de Goiás (UFG), Goiânia – GO – Brasil  
Emails: francielimoreira@discente.ufg.br, jonasjunior@discente.ufg.br, brakes_fares@discente.ufg.br, victorguerreiro@discente.ufg.br

## Resumo
Este trabalho propõe o desenvolvimento de um robô utilizando Turtlebot para auxiliar na distribuição de medicamentos em hospitais. O robô será programado para entregar medicamentos específicos para cada paciente conforme configurado pela enfermeira, evitando obstáculos durante sua rota.

**Palavras-chave**: robótica, Turtlebot, hospitais, distribuição de medicamentos, detecção de obstáculos.

## I. Introdução e Revisão Bibliográfica

### A. Problema
A distribuição de medicamentos em hospitais é uma atividade fundamental para o tratamento eficaz dos pacientes, mas também apresenta desafios significativos. A complexidade logística envolvida, desde a solicitação dos medicamentos pelos médicos até a administração correta aos pacientes, torna esse processo propenso a erros e atrasos. Além disso, a carga de trabalho dos profissionais de saúde, que já enfrentam demandas intensas, pode ser agravada pela necessidade de realizar essa distribuição manualmente, resultando em exaustão e possível comprometimento da segurança do paciente devido a erros humanos.

Diante desses desafios, a implementação de soluções para otimizar a distribuição de medicamentos em hospitais é de suma importância. O uso de robôs, como o Turtlebot, oferece uma abordagem promissora para automatizar parte desse processo, proporcionando maior eficiência, precisão e segurança. Ao explorar o potencial do Turtlebot na entrega de medicamentos, este projeto visa não apenas melhorar a qualidade do atendimento ao paciente, mas também reduzir a carga de trabalho dos profissionais de saúde e garantir uma administração precisa e oportuna dos medicamentos, contribuindo assim para a melhoria dos resultados clínicos e a segurança dos pacientes em ambientes hospitalares.

### B. Literatura
Para a revisão bibliográfica, foram selecionadas cinco fontes de informação relevantes sobre o tema:

1. **"Robots in Healthcare: a Scoping Review"** da Current Robotics Reports. Este estudo fornece uma revisão abrangente sobre os tipos de robôs utilizados em cuidados de saúde e os avanços tecnológicos que permitem que esses robôs realizem tarefas complexas, incluindo algoritmos de navegação e detecção de obstáculos. Disponível em: [ResearchGate](https://www.researchgate.net/publication/364641321_Robots_in_Healthcare_a_Scoping_Review)

2. **"Robots Speed Delivery of Meds in Hospitals"**. Esta matéria descreve como robôs de entrega de medicamentos são usados para otimizar a distribuição em hospitais, economizando tempo dos farmacêuticos e permitindo que se concentrem em outras tarefas essenciais. O artigo destaca exemplos específicos de implementação e os benefícios percebidos pelos profissionais de saúde. Disponível em: [ASHP](https://news.ashp.org/news/feature-stories/2023/11/14/robots-speed-delivery-of-meds-in-hospitals)

3. **"Mercy to deploy a fleet of robots throughout hospitals in 2023"** da Becker's Hospital Review. A matéria discute a implementação de uma frota de robôs em hospitais para tarefas de suporte, como a entrega de medicamentos, ressaltando a eficiência e a integração com os sistemas hospitalares existentes. Disponível em: [Becker's Hospital Review](https://www.beckershospitalreview.com/innovation/mercy-to-deploy-a-fleet-of-robots-throughout-hospitals-in-2023.html)

4. **"Six Robots Helping Doctors Today"**. Esta matéria explora várias inovações em robótica médica, incluindo o uso de machine learning para melhorar a precisão e eficiência dos robôs nas tarefas críticas em ambientes de saúde. Disponível em: [ASME](https://www.asme.org/topics-resources/content/six-robots-helping-doctors-today)

5. **"Sistema De Distribuição De Medicamentos Hospitalar"**. Este vídeo explica como funciona o sistema de distribuição de medicamentos hospitalares e aborda os principais problemas enfrentados. Disponível em: [YouTube](https://www.youtube.com/watch?v=9mLIYlE7PWg)

### C. Dataset
Os dados a serem explorados neste projeto incluem informações detalhadas sobre o ambiente hospitalar, os medicamentos e as interações entre o robô e os usuários. Aqui estão os principais componentes do dataset:

- **Dados de Sensores**: Dados coletados pelos sensores do TurtleBot, como LiDAR (Light Detection and Ranging) e câmeras, para a criação de mapas em tempo real e ajuste de rotas.
- **Dados de Simulação**: Gerados em ambientes simulados, como o Gazebo, para testar algoritmos de navegação e detecção de obstáculos em cenários controlados.
- **Layouts e Plantas Baixas**: Mapas dos hospitais serão coletados para auxiliar no planejamento das rotas. Estes mapas incluirão informações sobre a disposição dos quartos, corredores, áreas de armazenamento de medicamentos, e outros pontos de interesse.
- **Histórico de Entregas**: Informações sobre cada entrega realizada, incluindo horário de início e término, localização de coleta e entrega, e identificação do medicamento.
- **Tempos de Entrega**: Dados sobre o tempo total gasto em cada entrega, incluindo tempo de deslocamento e tempo de interação com os profissionais de saúde.

### D. Métodos
Os métodos revisados incluirão:

- **Navegação Autônoma**: Algoritmos que permitem ao robô criar um mapa do ambiente e ao mesmo tempo determinar sua localização dentro desse mapa. O uso de SLAM é crucial para que o TurtleBot possa se mover de forma autônoma e evitar obstáculos.
- **Planejamento de Rotas**: Algoritmos de planejamento de rotas para garantir a entrega eficiente e precisa dos medicamentos.
- **Reconhecimento de Objetos**: Uso de técnicas de visão computacional para identificar medicamentos e outras referências visuais importantes no ambiente hospitalar.
- **Simulação e Treinamento**: Utilização de ambientes simulados para treinar o robô antes da implementação no ambiente real.

### E. Avaliação
O impacto dos resultados será medido através das seguintes métricas:

- **Taxa de Sucesso nas Entregas**: Percentual de entregas realizadas corretamente e dentro do tempo estipulado.
- **Tempo de Entrega**: Tempo médio necessário para completar uma entrega.
- **Precisão na Navegação**: Acurácia do robô ao seguir as rotas planejadas e evitar obstáculos.
- **Feedback dos Usuários**: Nível de satisfação dos profissionais de saúde com o desempenho do robô.
- **Redução de Erros Humanos**: Comparação da taxa de erros antes e depois da implementação do robô.

## III.  Metodologia
Esta seção explica o processo metodológico para desenvolver o sistema de entrega de medicamentos utilizando o robô TurtleBot, com ênfase na integração de um site em Streamlit que serve como interface para entrada de ordens de medicamentos e na comunicação dessas ordens ao robô através de uma API.

### A. Planejamento e Design
- **Identificação de Requisitos**: Definição dos requisitos do sistema, incluindo as funcionalidades necessárias para a navegação do robô e a interação com o site em Streamlit.
- **Design do Sistema**: Elaboração do design do robô TurtleBot integrado com um site desenvolvido em Streamlit, que serve como interface para o pedido de medicamentos. Este design considera não só a navegação autônoma e a entrega física dos medicamentos, mas também a interface digital para entrada de pedidos e o backend para processamento dessas ordens.

### B. Desenvolvimento de Software

- **Interface segura de login para médicos:** :Utilizando práticas robustas de segurança como criptografia de senhas e autenticação multifator. Formulário web para pedidos de medicamentos, incluindo campos para identificação do paciente, seleção de medicamento, dosagem, instruções especiais e urgência do pedido. Esta funcionalidade centraliza e simplifica o processo de prescrição de medicamentos.
- **Integração com o Sistema do Hospital** : Mecanismos para integrar o site com os sistemas existentes do hospital, como sistemas de gerenciamento de pacientes e de estoque de medicamentos. Assegurar que as informações de identificação do paciente e os dados de estoque estejam sempre atualizados, permitindo uma operação mais eficiente e precisa.
- **Processamento de Pedidos** : Criação de uma API que comunica diretamente com o robô TurtleBot para processar e entregar os pedidos de medicamentos de forma automatizada. Implementação de funcionalidades para revisão e confirmação dos pedidos antes de serem enviados ao robô, garantindo que todos os detalhes estejam corretos e completos.
- **Desenvolvimento de Localização, Percepção e Navegação do Robô Utilizando ROS2:** : Implementação de algoritmos de localização para determinar a posição do robô dentro do ambiente hospitalar, utilizando sensores como LIDAR e câmeras. Desenvolvimento de funcionalidades de percepção para detecção de obstáculos e identificação de rotas seguras. Navegação autônoma do robô para entrega dos medicamentos, incluindo planejamento de trajetórias e controle de movimento, garantindo a entrega eficiente e segura dos medicamentos.

### C. Simulação e Testes
- **Configuração do Ambiente Simulado no Gazebo**: Simulação para testar a navegação e entrega do medicamento do TurtleBot.
- **Testes de Integração**: Verificação da comunicação eficiente entre o site Streamlit, a API, e o robô. Testes para garantir que as ordens de medicamentos sejam processadas corretamente pelo robô. E se a rota e navegação estão de acordo com o local de entrega.

### D.  Implementação e Avaliação
- **Implementação no Ambiente Real**: Implantação do robô TurtleBot no hospital, iniciando as operações de entrega baseadas nas ordens recebidas através do site Streamlit.
- **Monitoramento e Coleta de Dados**: Monitoramento contínuo para coletar dados sobre a precisão e a eficiência das entregas, bem como a usabilidade do site Streamlit.
- - **Avaliação do Desempenho**:Análise dos dados testes realizados para avaliar o sucesso das entregas, a integridade da comunicação via API e a possível satisfação dos usuários com a interface do site.
