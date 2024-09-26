# Envio de Dados para Porta Serial
# Descrição
Este projeto visa construir uma programação básica que interpreta o estado lógico de um botão. Com base nesta ideia o usuário pode adentrar-se ao mundo de coleta de dados externo e leitura interna pelo arduino, podendo então construir vários outros projetos de propósito do usuário.
# Funcionamento
- **Botão está Pressionado:** Quando o botão está sendo pressionado aparece, no campo de Porta Serial do Arduino IDE, o estado lógico do botão, que neste caso é alto.
- **Botão não está Pressionado:** Quando o botão não está sendo pressionado aparecerá que o botão está no estado baixo. Poderemos ver essa analise através da Porta Serial do Arduino IDE.

Além disso, pode-se inverter os estados lógicos. Quando o botão for pressionado aparecerá que está em estado baixo, mas se for solto aparecerá que está em alto. Para fazer isso basta inverter os comandos na programação do arduino.
# Materiais Necessários
- 1 Arduino UNO
- 1 Protoboard
- 1 Botão de Pressão
- 1 Resistor de 10KΩ (pull-up)
- Fios de Conexão (jumpers)
# Montagem do Circuito
**1. Conectar o Botão**
  - Encaixe o botão no Protoboard de modo que dois de seus terminais estejam do lado leste, e e os outros dois terminais, do lado oeste do protoboard.
  - Conecte o GND (0V) a um terminal do botão, e do mesmo lado conecte o VCC (5V) ao outro terminal usando um resistor de 10KΩ.
  - Do outro lado, mas de terminal oposto ao VCC conecte um fio jumper ligando ao pino digital 2 do arduino.
