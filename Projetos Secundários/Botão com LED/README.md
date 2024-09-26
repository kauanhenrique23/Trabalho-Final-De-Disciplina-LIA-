# LED com Botão
# Descrição 
O intuito deste projeto é fazer um LED acender a parir de um botão. A programação necessário para se produzir este projeto é altamente básica. A partir da ideia utilizada neste projeto, o interessado poderá expandir esta ideia e fazer o seu próprio projeto sobre qualquer coisa.
# Funcionamento
- **Botão não pressionado:** Quando o botão não está pressionado o pino de entrada digital 2 do aruino interpreta como LOW (0V) a entrada. Assim enviando um pulso LOW (0V) para a saída digital do pino 12 do arduino, não acendendo o LED.
- **Botão pressionado:** Quando o botão está pressionado o pino de entrada digital 2 do arduino interpreta como HIGH (5V) a entrada. Assim enviando um pulso HIGH (5V) para a sáida digital do pino 12 do arduino, acendendo o LED.

Além disso, é possível inverter a ideia do projeto, basta inverter o comando que acontece quando se está HIGH (5V) pelo comando LOW (5V) e vice-versa na programação do arduino. Assim o LED ficará aceso até o botão ser pressionado e apagá-lo.
# Materias Necessários
- **1 Arduino UNO**
- **1 Protoboard**
- **Fios de Conexão (jumpers)**
- **2 Resistores 10KΩ (pull-up)**
- **1 Botão de Pressão**
- **1 LED**
# Montagem do Circuito
**1. Conectar o Botão**
  - Usando um Protoboard, encaixe um botão de pressão em seu meio com dois terminais de um lado e dois terminais de outro lado.
  - De um lado do botão conecte o GND (0V) e o VCC (5V) (o VCC deverá ser concectado com um resistor de 10KΩ) por fios jumpers.
  - Do outro lado conecte um fio jumper ao pino digital 2 do arduino (lembre - se de conectar no terminal inverso ao colocado no VCC).

**2. Conectar o LED**
  - No mesmo Protoboard, encaixe o LED. Lembre-se o terminal maior é o positivo (VCC) e o menor, o negativo (GND).
  - Coloque cada terminal em uma linha diferente.
  - Ligue, com um fio jumper, o pino digital 12 do arduino ao VCC do LED (terminal maior) a partir de um resistor de 10KΩ.
  - Conecte o GNG (terminal menor) do LED ao GND do arduino com um fio jumper.
