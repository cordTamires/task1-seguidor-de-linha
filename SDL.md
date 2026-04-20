# Seguidor de linha
- O que é 
-  Principais componentes

Um seguidor de linha é um robô móvel de alta perfomance projetado para se deslocar automaticamente seguindo um trajeto marcado no chão, geralmente uma linha branca 
sobre fundo preto. Ele funciona detectando essa linha por meio de sensores e ajustando continuamente o movimento das rodas para permanecer sobre o caminho.

**Principais componentes:**
- Microcontrolador.
Ele é como a central de controle do robô, ele manda e recebe comunicação dos seus componentes conectado. Lê os dados dos sensores, processa essas informações e decide como os motores devem agir (virar, ir reto, corrigir rota).

---

2. Buck Converter

É responsável por fornecer a tensão adequada para os diferentes componentes do robô. Ele converte a tensão da bateria para níveis adequados, mantendo a eficiência energética.
  
### Necessidade:
- O robô precisa de uma fonte de alimentação estável e eficiente. A maioria dos componentes eletrônicos do sistema, como o ESP32 e os sensores, opera em tensões diferentes da bateria principal. O buck converter assegura que os componentes recebam as tensões corretas sem desperdiçar energia.

### Requisitos:
- **Tensão de entrada**: Compatível com a tensão da bateria do robô (geralmente entre 7,4V e 12V).
- **Tensão de saída**: Saídas de 5V e 3,3V.
- **Corrente de saída**: Capacidade para fornecer pelo menos 2A para os componentes.
  
---

3. Switch On/Off

### Quantidade:
- 1 unidade

### Especificações de Uso:
- **Chave liga/desliga**: Será utilizada para controlar o fornecimento de energia do sistema. Isso permite o desligamento completo do robô sem a necessidade de desconectar a bateria.

### Necessidade:
- Em uma competição, é essencial poder ligar e desligar o robô de forma rápida e segura. Um switch on/off permite a gestão eficiente da energia durante os intervalos das provas.

### Requisitos:
- **Tensão de operação**: Compatível com a bateria do robô (7,4V a 12V).
- **Corrente suportada**: Pelo menos 5A, para evitar aquecimento ou falhas com picos de corrente dos motores.

---
4. Motores 3000 RPM 6V Polulu com Encoder Genérico
### Quantidade:
- 2 unidades (para movimentação do robô)

### Especificações de Uso:
- **Motores DC**: Os motores com encoder permitem controlar a velocidade e o sentido de rotação com precisão. A rotação máxima de 3000 RPM oferece velocidade suficiente para percorrer a pista com eficiência.
- **Encoder**: O encoder embutido fornece feedback da posição e velocidade do motor, essencial para controlar com precisão a movimentação do robô e realizar ajustes finos na trajetória.
  
### Necessidade:
- Os motores são responsáveis pela propulsão do robô. O uso de encoders ajuda a garantir o controle fino da velocidade e a capacidade de ajustar a direção e manter o robô na trajetória correta.

### Requisitos:
- **Tensão de operação**: 6V
- **Corrente de operação**: 1,5A (nominal), até 3A (em pico)
- **Tipo de Encoder**

: Incremental, com resolução mínima de 10 pulsos por rotação.
  
---

5. Ponte H DRV8833
### Quantidade:
- 1 unidade

### Especificações de Uso:
- **Driver de motor**: A ponte H DRV8833 permite o controle de dois motores DC de forma independente, controlando a direção e a velocidade através de sinais PWM. Ela protege os circuitos de controle e permite um controle eficaz da movimentação dos motores.

### Necessidade:
- Este componente é essencial para controlar os motores, uma vez que o ESP32 não pode fornecer corrente suficiente para os motores diretamente. A ponte H também permite mudar a direção dos motores rapidamente, o que é crucial para as curvas e ajustes de direção durante a competição.

### Requisitos:
- **Tensão de operação**: 4,5V a 13,5V
- **Corrente máxima por canal**: 1,2A (contínuo), 3,2A (pico)
- **Entradas de controle**: PWM, IN1/IN2 para direção, STBY para ativação/desativação.

---

6. Sensor Lateral QRE1113

### Quantidade:
- 2 unidades (um para cada lado do robô)

### Especificações de Uso:
- **Sensores infravermelhos ou ultrassônicos**: Os sensores laterais são usados para detectar obstáculos ou bordas laterais da pista. Podem ser usados sensores infravermelhos de distância curta ou ultrassônicos, dependendo do tipo de pista.

### Necessidade:
- Os sensores laterais auxiliam o robô a evitar colisões e a manter-se centralizado na pista. São fundamentais para estratégias avançadas, como desviar de obstáculos ou manter uma distância ideal das bordas laterais.

### Requisitos:
- **Tensão de operação**: 5V
- **Distância de detecção**: 2 a 10 cm para infravermelho ou 2 a 30 cm para ultrassônico.
- **Saída**: Sinal digital ou analógico para leitura pelo ESP32.

---

7. Módulo de 8 Sensores Frontal QRE1113
### Quantidade:
- 1 unidade

### Especificações de Uso:
- **Array de sensores infravermelhos**: O módulo de sensores será responsável pela detecção da linha que o robô deve seguir. O conjunto de 8 sensores infravermelhos permite uma leitura precisa da posição da linha em relação ao robô, garantindo um controle fino da trajetória.

### Necessidade:
- O array de sensores é o principal componente que permite ao robô seguir a linha. A precisão deste módulo é crítica para garantir que o robô seja capaz de seguir a linha de forma suave e reagir rapidamente a mudanças no trajeto.

### Requisitos:
- **Tensão de operação**: 5V
- **Tipo de sensor**: Infravermelho (IR) para detecção de contraste.
- **Saída**: 8 sinais digitais ou analógicos, indicando a presença da linha sob cada sensor.
- **Largura de detecção**: Deve cobrir a largura total da pista, com sensores espaçados uniformemente para garantir uma leitura estável.

