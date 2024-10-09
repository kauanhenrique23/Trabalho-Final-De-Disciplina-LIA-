# Contagem de Pressionamentos de Botão

# Descrição
Este projeto visa construir um mecanismo simples com botão, através de uma básica programação, capaz de detectar e contar quantas vezes o botão foi pressionado. Com base neste projeto, o usuário será capaz de expandir esta ideia a vários outros projetos de uso próprio da forma que bem entender.

# Funcionamento
- **Botão não Pressionado:** Quando o botão não está sendo pressionado aparecerá a palavra "off" (caractere usado na programação) no monitor serial do Arduino IDE.
- **Botão Pressionado:** A cada vez que o botão for pressionado somará 1 ao número de pressionamento anteriores. Assim formando uma contagem de pressionamentos automática.

# Materiais Necessários
- 1 Arduino UNO
- 1 Protoboard
- 1 Resistor 10KΩ (pull-up)
- 1 Botão de Pressão
- Fios de Conexão (jumpers)
# Montagem do Circuito

**1. Conectar o Botão**
  - Encaixe o botão no Protoboard de modo que dois terminais fiquem do lado esquerdo e os outros dois, do lado direito do Protoboard.
  - De um lado conecte o VCC (5V) e o GND (0V), de modo que o VCC seja conectado através de um resistor de 10KΩ.
  - Do outro lado conecte um terminal ao pino digital 2 do arduino através de um fio jumper (lembre-se de conectá-lo ao terminal oposto do terminal onde o VCC (5V) foi conectado).
