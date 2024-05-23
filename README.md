
# Conteúdo de Estudo para Redes de Computadores II

Este documento abrange conceitos fundamentais de Redes de Computadores II, com foco nas aulas sobre a Camada Física. A seguir, uma explicação detalhada dos principais tópicos abordados.

<details>
  <summary>Aula 07 - Dados e Sinais, Perdas na Transmissão</summary>

  ### Dados e Sinais

  **Características das Ondas Senoidais**:
  - **Amplitude (A)**:
    - Define a altura máxima da onda em relação ao seu valor médio.
    - Medida em volts (V), representa a intensidade ou potência do sinal.
    - Exemplo: Uma onda com amplitude de 5V atinge um pico de +5V e -5V.

  - **Frequência (f)**:
    - Número de ciclos completos que uma onda realiza em um segundo.
    - Medida em hertz (Hz).
    - Fórmula: `f = 1/T`, onde `T` é o período (tempo para completar um ciclo).
    - Exemplo: Se uma onda completa um ciclo em 0.01 segundos, sua frequência é 100 Hz.

  - **Fase (θ)**:
    - Deslocamento da onda no tempo em relação a um ponto de referência.
    - Medida em graus ou radianos.
    - Define onde a onda começa em seu ciclo.
    - Exemplo: Duas ondas com a mesma amplitude e frequência, mas com fases diferentes, começarão em pontos diferentes no tempo.

  **Contribuição de Joseph Fourier**:
  - Fourier demonstrou que qualquer sinal periódico pode ser representado como uma soma de ondas senoidais (série de Fourier).
  - Isso significa que sinais complexos podem ser decompostos em suas componentes senoidais básicas.
  - **Transformada de Fourier**: Ferramenta matemática usada para transformar um sinal do domínio do tempo para o domínio da frequência.
    - Aplicações incluem análise de sinais, processamento de imagem e compressão de dados.

  **Sinais Compostos e Não Periódicos**:
  - **Sinais compostos**: Compostos por múltiplas frequências.
    - Exemplo: Um sinal quadrado pode ser decomposto em uma série infinita de senóides.
  - **Sinais não periódicos**: Não se repetem em intervalos regulares.
    - A análise de Fourier pode ser estendida para sinais não periódicos usando a Transformada de Fourier.

  **Largura de Banda**:
  - Diferença entre a frequência máxima e mínima que um canal pode transmitir.
  - Representa a capacidade do canal de transmitir informações.
  - Exemplo: Se um canal pode transmitir frequências de 1 kHz a 5 kHz, sua largura de banda é 4 kHz.

  ### Transmissão de Sinais Digitais

  **Transmissão Banda-base**:
  - Utiliza toda a largura de banda do meio de transmissão para um único sinal digital.
  - Comum em redes locais (LANs), como Ethernet.
  - **Sinal digital**: Representa dados em formato binário (0s e 1s).

  **Canais Passa-faixa, Passa-alta e Passa-baixa**:
  - **Passa-faixa**: Permite apenas uma faixa específica de frequências passar.
    - Exemplo: Comunicação via rádio, onde uma faixa específica é atribuída a cada estação.
  - **Passa-alta**: Permite apenas frequências acima de um certo valor.
    - Exemplo: Filtros de áudio que removem ruídos de baixa frequência.
  - **Passa-baixa**: Permite apenas frequências abaixo de um certo valor.
    - Exemplo: Filtros que removem ruídos de alta frequência em sinais de áudio.

  **Reconstrução do Sinal**:
  - Problema de garantir que o sinal digital recebido seja uma representação fiel do sinal transmitido.
  - **Amostragem**: Processo de medir o valor do sinal em intervalos regulares.
    - Regra de Nyquist: Para evitar aliasing, a taxa de amostragem deve ser pelo menos duas vezes a frequência máxima do sinal.
  - **Filtragem**: Remove ruídos e distorções do sinal recebido.

  ### Perdas na Transmissão

  **Atenuação**:
  - Perda de intensidade do sinal à medida que ele se propaga.
  - Causada por resistência do material e dispersão do sinal.
  - Exemplo: Sinais em cabos coaxiais se enfraquecem ao longo da distância.

  **Distorção**:
  - Ocorre quando diferentes componentes de frequência de um sinal viajam a velocidades diferentes.
  - Resulta em alteração da forma do sinal original.
  - Exemplo: Distorção de fase em redes de comunicação pode causar erros de dados.

  **Ruído**:
  - Interferências indesejadas que degradam o sinal.
  - Tipos de ruído:
    - **Ruído térmico**: Gerado pelo movimento de elétrons em condutores.
    - **Ruído de intermodulação**: Causado pela combinação de sinais diferentes.
    - **Ruído impulsivo**: Causado por eventos súbitos, como relâmpagos.

</details>

<details>
  <summary>Aula 08 - Transmissão Analógica</summary>

  ### Modulação de Sinais Digitais

  **ASK (Amplitude Shift Keying)**:
  - A amplitude da portadora é variada de acordo com o sinal digital.
  - **ASK Binário**: Utiliza dois níveis de amplitude para representar 0 e 1.
  - **Vantagem**: Simplicidade de implementação.
  - **Desvantagem**: Alta suscetibilidade ao ruído, pois qualquer variação na amplitude pode ser interpretada como erro.

  **FSK (Frequency Shift Keying)**:
  - A frequência da portadora é variada de acordo com o sinal digital.
  - **BFSK (Binary FSK)**: Utiliza duas frequências diferentes para representar 0 e 1.
  - **Vantagem**: Menos suscetível ao ruído em comparação ao ASK.
  - **Desvantagem**: Requer maior largura de banda.

  **PSK (Phase Shift Keying)**:
  - A fase da portadora é variada para representar os dados.
  - **BPSK (Binary PSK)**: Utiliza duas fases diferentes para representar 0 e 1.
  - **QPSK (Quadrature PSK)**: Utiliza quatro fases diferentes, aumentando a eficiência de transmissão.
  - **Vantagem**: Maior eficiência espectral.
  - **Desvantagem**: Complexidade de implementação.

  **QAM (Quadrature Amplitude Modulation)**:
  - Combinação de ASK e PSK, variando tanto a amplitude quanto a fase da portadora.
  - Permite transmitir mais bits por símbolo.
  - **Vantagem**: Alta eficiência espectral.
  - **Desvantagem**: Mais suscetível ao ruído e interferência.

  **Diagrama de Constelação**:
  - Representação gráfica dos estados de modulação de um sinal.
  - Eixo horizontal (I) representa a componente em fase.
  - Eixo vertical (Q) representa a componente em quadratura.
  - Ajuda a visualizar a separação entre diferentes estados de modulação e a tolerância a erros.

  ### Meios Físicos de Transmissão

  **Guiados vs. Não-Guiados**:
  - **Meios Guiados**:
    - **Par Trançado**: Dois fios entrelaçados para reduzir interferências eletromagnéticas.
      - **UTP (Unshielded Twisted Pair)**: Sem blindagem adicional.
      - **STP (Shielded Twisted Pair)**: Com blindagem para proteção extra.
    - **Cabo Coaxial**: Um fio condutor central rodeado por um isolante e uma malha condutora.
      - Alta capacidade de largura de banda.
      - Usado em redes de televisão a cabo e internet.
    - **Fibra Óptica**: Utiliza luz para transmitir dados através de um núcleo de vidro ou plástico.
      - **Vantagens**: Alta capacidade de transmissão, imunidade a interferências eletromagnéticas, e menor atenuação.
      - **Desvantagens**: Custo mais alto e necessidade de equipamentos especializados para instalação e manutenção.

  - **Meios Não-Guiados**:
    - **Rádio**: Transmissão sem fio usando ondas de rádio.
      - Usado em redes Wi-Fi, Bluetooth, e comunicação celular.
    - **Micro-ondas**: Transmissão de alta frequência usada em enlaces ponto a ponto e satélites.
      - **Vantagem**: Capacidade de cobrir grandes distâncias.
      - **Desvantagem**: Suscetível a obstruções físicas e interferências atmosféricas.
    - **Infravermelho**: Usado para comunicação de curto alcance, como controles remotos e comunicação entre dispositivos próximos.

</details>

# Guia de Estudo para Redes de Computadores II

Este guia de estudo foi elaborado com base na lista de exercícios fornecida pelo Prof. Dr. Tiago B. N. Silveira para a disciplina de Redes de Computadores II, 2024.1, do curso de Ciência da Computação. O objetivo é ajudar a compreender os principais conceitos abordados na matéria, focando nas questões da lista de exercícios.

<details>
  <summary>Unidade 1: Camada de Enlace (VLANs e MPLS)</summary>

  ### 1. Conexão de switches com VLANs
  **Questão**: Quantas portas serão necessárias para conectar N switches que suportam K grupos de VLAN?

  **Conceito**: VLAN (Virtual Local Area Network)
  - **VLANs** permitem a segmentação lógica de uma rede física em diferentes domínios de broadcast. Isso significa que você pode separar o tráfego de rede de diferentes departamentos ou grupos dentro de uma empresa, mesmo que todos estejam usando o mesmo hardware de rede.
  - **Protocolo de entroncamento (trunking)**: É utilizado para transportar tráfego de múltiplas VLANs através de uma única conexão entre switches. O protocolo mais comum é o IEEE 802.1Q.

  **Resolução**:
  - Se tivermos N switches, e cada um deve se comunicar com os outros, geralmente cada switch precisa de uma porta de entroncamento para cada conexão com outro switch. Assim, cada switch precisaria de \((N-1)\) portas.
  - Exemplo: Para 4 switches (N = 4), cada switch precisará de 3 portas para se conectar aos outros três switches.

  ### 2. VLANs em empresas
  **Questão**: Como uma VLAN pode poupar tempo e dinheiro para uma empresa?

  **Conceito**: 
  - **Segmentação lógica**: Reduz a necessidade de reconfiguração física da rede ao mudar departamentos ou grupos de trabalho, economizando tempo de administração.
  - **Eficiência de rede**: Melhora a utilização da largura de banda ao limitar os domínios de broadcast.
  - **Custo**: Reduz a necessidade de hardware adicional, como switches separados para cada departamento.

  ### 3. Segurança das VLANs
  **Questão**: Como uma VLAN fornece segurança adicional para uma rede?

  **Conceito**: 
  - **Isolamento**: Cada VLAN é um domínio de broadcast separado. Dispositivos em VLANs diferentes não podem se comunicar diretamente a menos que seja permitido pelo roteamento entre VLANs.
  - **Controle de acesso**: Políticas de segurança podem ser aplicadas a VLANs específicas, restringindo acesso a recursos sensíveis.

  ### 4. Engenharia de tráfego em MPLS
  **Questão**: Como configurar tabelas MPLS para direcionar tráfego específico através de rotas diferentes?

  **Conceito**: MPLS (Multiprotocol Label Switching)
  - MPLS é uma técnica usada para encaminhamento eficiente de pacotes em uma rede através da adição de labels aos pacotes.
  - **Tabela de comutação de labels (LSR - Label Switching Router)**: Define as ações a serem tomadas com base nos labels.

  **Resolução**:
  - Suponha que queremos que pacotes de R6 para A sejam encaminhados via R6-R4-R3-R1 e pacotes de R5 para A via R5-R4-R2-R1. Configuramos as tabelas MPLS nos roteadores R5, R6 e R4 para refletir essas rotas.

  ### 5. Etapas de protocolo para acessar uma página web
  **Questão**: Quais são as etapas de protocolo desde ligar o computador até receber uma página web?

  **Conceito**:
  - **Ethernet**: Estabelece a conexão física.
  - **DHCP (Dynamic Host Configuration Protocol)**: Obtém um endereço IP.
  - **ARP (Address Resolution Protocol)**: Obtém o endereço MAC do roteador.
  - **DNS (Domain Name System)**: Resolve o nome de domínio em um endereço IP.
  - **TCP (Transmission Control Protocol)**: Estabelece uma conexão confiável.
  - **HTTP (HyperText Transfer Protocol)**: Faz a solicitação e recebe a página web.

  **Resolução**:
  1. **Ethernet**: Conecta o computador à rede local.
  2. **DHCP**: O computador solicita um endereço IP de um servidor DHCP.
  3. **ARP**: O computador usa ARP para descobrir o endereço MAC do roteador.
  4. **DNS**: O computador envia uma solicitação DNS para resolver o nome de domínio do site para um endereço IP.
  5. **TCP**: Estabelece uma conexão TCP com o servidor web.
  6. **HTTP**: Envia uma solicitação HTTP para obter a página web.

</details>

<details>
  <summary>Unidade 2: Camada Física</summary>

  ### 6. Período e frequência de um sinal
  **Questão**: Qual é a relação entre período e frequência de um sinal?

  **Conceito**:
  - **Período (T)**: Tempo que um ciclo completo de um sinal leva para ocorrer.
  - **Frequência (f)**: Número de ciclos completos que ocorrem em um segundo.
  - **Relação**: \( f = \frac{1}{T} \).

  ### 7. Medidas de amplitude, frequência e fase
  **Questão**: O que mede a amplitude, a frequência e a fase de um sinal?

  **Conceito**:
  - **Amplitude**: Valor máximo do sinal (em volts).
  - **Frequência**: Número de ciclos por segundo (em hertz, Hz).
  - **Fase**: Deslocamento do início do ciclo (em graus).

  ### 8. Decomposição de sinal composto
  **Questão**: Como um sinal composto pode ser decomposto em suas componentes de frequências individuais?

  **Conceito**:
  - **Transformada de Fourier**: Decompõe um sinal em suas frequências componentes.

  ### 9. Tipos de perda na transmissão de sinais
  **Questão**: Cite os três tipos de perda na transmissão de sinais.

  **Conceito**:
  - **Atenuação**: Perda de intensidade do sinal ao longo da distância.
  - **Distorção**: Alteração da forma do sinal.
  - **Ruído**: Interferências que afetam a qualidade do sinal.

  ### 10. Transmissão banda-base vs. banda-larga
  **Questão**: Qual é a diferença entre transmissão banda-base e transmissão banda-larga?

  **Conceito**:
  - **Banda-base**: Utiliza toda a largura de banda do meio para um único sinal.
  - **Banda-larga**: Divide a largura de banda em múltiplos canais para transmitir múltiplos sinais simultaneamente.

</details>

## Conclusão

Este guia aborda os conceitos fundamentais de VLANs, MPLS e a camada física, conforme requerido na lista de exercícios. Ao entender esses conceitos, você estará bem preparado para a prova, que consiste em 80% de questões de múltipla escolha e 20% de questões descritivas.

Para dúvidas ou mais informações, consulte o material recomendado pelo professor e pratique os exercícios.

Boa sorte nos estudos!
