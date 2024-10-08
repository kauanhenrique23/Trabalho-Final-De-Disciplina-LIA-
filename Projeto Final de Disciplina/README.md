# Robô Desviador de Obstáculos
Versão 1.0 Plataforma: Arduino UNO
## Componentes Utilizados
- **Arduino Uno**

    Microcontrolador responsável por coordenar o movimento dos dois motores simultaneamente através de uma programação simples.
- **Protoboard**

    Onde serão colocados o Medidor Ultrassônico e os fios para sua conexão.
- **Módulo de Motor Ponte H dupla L298N**

    A partir da programação estabelecida na Arduino IDE, é responsável pela coordenação do movimento dos motores.
- **Chassi**

    O chassi servirá de suporte para o encaixe de todos os componentes necessários no projeto.

- **2 Motor DC 3-6V**

    Os motores serão responsáveis por fazer a roda girar sendo controlados pelo Módulo de Motor.

- **2 Rodas**

    As rodas dão suporte ao chassi facilitando seu transporte. Os motores DC que as fazem girar.

- **Bateria 9V**

    Responsável por alimentar o Arduino Uno, já  que não estará conectado a nenhuma outra fonte externa.

- **Suporte para 4 Pilhas 1,5V**

    Servirão de fonte de alimentação para os dois motores. Nao é necessário para um projeto completo.

- **1 Rodinha de Gel Giratória**

    Servirá de suporte para manter o chassi reto e em pé.

- **Fios de Conexão(jumpers)**

    Serão necessários para se fazer todas as conexões.

- **Módulo Sensor de Distância Ultrassônico HC-SR04**

    Esse sensor envia pulsos ultrassônicos e os recebe de volta, possibilitando a captura de dados de distância à um obstáculo em sua frente.

## Descrição
Este projeto implementa um robô de duas rodas mecânicas ligadas a um eixo de um motor e uma roda giratória atrás (ou na frente), que através de m medidor ultrassônico, o ajuda a não esbarrar em nenhuma estrutura que estiver em seu caminho. Isso tudo sem nenhum controle de fora, totalmente automático e de uso prático, sendo ideal para exposições de robótica.

### Funcionamento 
**1. Captação de Dados**

  **- Módulo Sensor de Distância Ultrassônico HC-SR04:** 
  
- **Conexão:** Para se fazer a conexão do Sensor Ultrassônico ao Arduino serão necessários 4 fios jumpers macho-macho. O componente de que se trata apresenta quatro pinos que devem ser encaixados no Protoboard de forma que cada pino fique localizado em uma linha horizontal diferente. O primeiro pino, da esquerda para a direita, é o pino VCC (5V) e deve ser conectado ao 5V do Arduino; o segundo pino, chamado Trigger, deve ser conectado à um pino digital do Arduino da preferência do usuário; o terceiro pino, chamado Echo, deve ser conectado a outro pino digital diferente do conectado ao segundo pino; o quarto pino é o GND (0V) e deve ser conectado ao próprio GND do Arduino.
- **Funcionamento:** O sensor envia um pulso ultrassônico, em seguida a onda é bloqueada por algum possível obstáculo e é retornada. O Arduino usa esse tempo de ida e volta, e com base na fórmula: *Distância  = (Tempo de duração do sinal de saída × velocidade do som) / 2)*, será possível saber a distância entre o medidor ultrassônico e um obstáculo à sua frente, pois como sabemos a velocidade do som (pulso ultrassônico) que corresponde a exatamente 340 m/s; e o tempo de duração (ida e volta), posteriormente será possível calcular a distância.

**2. Estrutura Mecânica**

  **- Motores**

- **Conexão:** Usando o Módulo de Motor L298N é possível fazer o controle de 2 motores simultaneamente, conectando o positivo e negativo do motor A ao OUT1 e OUT2; e do motor B ao OUT3 e OUT4. Lembre-se sempre de fazer um padrão: se colocar no OUT1 o polo positivo do motor, coloque também no OUT3 o polo positivo do outro motor; se colocar o positivo no OUT2, coloque o positivo do outro motor no OUT4 e assim vice-versa.
- **Alimentação:** Para alimentar os motores será necessária uma fonte que poderá ser uma bateria de 9V usada para alimentar também o Arduino UNO; ou pilhas que possuem uma tensão entre 3 e 6 volts para os motores funcionarem normalmente. Conecte, através de cabos jumpers, o positivo da fonte ao encaixe de 12V do módulo e o negativo, ao GND. 
- **Controle:** Para fazer o controle do movimento dos motores (quando irão girar e para qual sentido) será necessário conectar 4 pinos digitais do Arduino quaisquer, respectivamente, às entradas IN1 e IN2(motor A), IN3 e IN4(motor B) do módulo. O movimento dos motores está diretamente ligado à que estados lógicos esses 4 pinos estão de acordo com a tabela abaixo:

![Imagem](https://github.com/user-attachments/assets/5e4278c6-b410-4580-91f8-dc3fdb7c9840)

**- Os dois possíveis esquemas elétricos que se podem usar para produzir este projeto:**

- [Esquema Elétrico 1 do Projeto](https://github.com/kauanhenrique23/Trabalho-Final-De-Disciplina-LIA-/blob/main/Projeto%20Final%20de%20Disciplina/Esquema%20Eletrico.png)
- [Esquema Elétrico 2 do Projeto](https://github.com/kauanhenrique23/Trabalho-Final-De-Disciplina-LIA-/blob/main/Projeto%20Final%20de%20Disciplina/Esquema%20El%C3%A9trico.png)

**3. Ideia do Programa:** 
  
- Agora que sabemos a distância, é só produzir um código em que quando a distância for menor que tal quantia, terá uma consequência, que por exemplo pode ser o robô ir para trás. E se a distância for maior, o robô irá fazer o contrário que no caso será ir para frente. Essa é a ideia em que todo este projeto é baseado; ela possui várias aplicações e o usuário poderá usá-la da maneira que quiser, para construir, assim, o seu projeto. 
- A distância utilizada neste projeto foi de 30 cm, mas através de testes de eficiência e coleta de dados, foi constatado que uma distância que faz manter uma boa eficiência do projeto deve estar entre 20 e 30 cm.
- Dentro deste diretório está presente todo o código usado neste projeto com instruções detalhadas para facilitar o entendimento do leitor. Para acessá-lo clique no link abaixo:

- [Códido do Projeto](https://github.com/kauanhenrique23/Trabalho-Final-De-Disciplina-LIA-/blob/main/Projeto%20Final%20de%20Disciplina/C%C3%B3digo.txt)

## Considerações Finais
Este projeto pode ser atribuído à várias aplicações no meio acadêmico e principalmente, no meio profissional. Em indústrias e fábricas,por exemplo, pode se expandir a tecnologia no uso de robôs automáticos que não precisam de nenhum tipo de operador para controlá-los. Com o uso de sensores ultrassônicos, facilita mais ainda o desenvolvimento dessas ideias. Por exemplo, carros que dirigem sozinhos podem ser construídos com o uso de arduino e alguns sensores. Essa nova tecnologia pode, e já está, transformando o mundo como conhecemos e vivemos.
