# Seguidor de linha
- O que é 
-  Principais componentes

Um seguidor de linha é um robô móvel de alta perfomance projetado para se deslocar automaticamente seguindo um trajeto marcado no chão, geralmente uma linha branca 
sobre fundo preto. Ele funciona detectando essa linha por meio de sensores e ajustando continuamente o movimento das rodas para permanecer sobre o caminho.

**Principais componentes:**
- Microcontrolador:
Ele é como a central de controle do robô, ele manda e recebe comunicação dos seus componentes conectado. Lê os dados dos sensores, processa essas informações e decide como os motores devem agir (virar, ir reto, corrigir rota).

---

- Buck Converter:

É responsável por fornecer a tensão adequada para os diferentes componentes do robô. Ele converte a tensão da bateria para níveis adequados, mantendo a eficiência energética. O robô precisa de uma fonte de alimentação estável e eficiente. A maioria dos componentes eletrônicos do sistema, como o ESP32 e os sensores, opera em tensões diferentes da bateria principal. O buck converter assegura que os componentes recebam as tensões corretas sem desperdiçar energia.

---

- Switch On/Off:
  
Será utilizada para controlar o fornecimento de energia do sistema. Isso permite o desligamento completo do robô sem a necessidade de desconectar a bateria. 
Permite a gestão eficiente da energia durante os intervalos das provas.

---
- Motores:

Os motores com encoder permitem controlar a velocidade e o sentido de rotação com precisão. A rotação máxima de 3000 RPM oferece velocidade suficiente para percorrer a pista com eficiência. Os motores são responsáveis pela propulsão do robô. O uso de encoders ajuda a garantir o controle fino da velocidade e a capacidade de ajustar a direção e manter o robô na trajetória correta.

---

- Ponte:

A ponte H  permite o controle de dois motores DC de forma independente, controlando a direção e a velocidade através de sinais PWM. Ela protege os circuitos de controle e permite um controle eficaz da movimentação dos motores. Este componente é essencial para controlar os motores, permite mudar a direção dos motores rapidamente, o que é crucial para as curvas e ajustes de direção durante a competição.

---

- Sensor Lateral:

Os sensores laterais são usados para detectar obstáculos ou bordas laterais da pista. Podem ser usados sensores infravermelhos de distância curta ou ultrassônicos, dependendo do tipo de pista. Os sensores laterais auxiliam o robô a evitar colisões e a manter-se centralizado na pista. São fundamentais para estratégias avançadas, como desviar de obstáculos ou manter uma distância ideal das bordas laterais.

---

- Módulo de 8 Sensores Frontal:

O módulo de sensores será responsável pela detecção da linha que o robô deve seguir. O conjunto de 8 sensores infravermelhos permite uma leitura precisa da posição da linha em relação ao robô, garantindo um controle fino da trajetória. O array de sensores é o principal componente que permite ao robô seguir a linha. A precisão deste módulo é crítica para garantir que o robô seja capaz de seguir a linha de forma suave e reagir rapidamente a mudanças no trajeto.



