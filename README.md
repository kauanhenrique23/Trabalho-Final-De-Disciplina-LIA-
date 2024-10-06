# Trabalho-Final-De-Disciplina-LIA
Versão 1.0 Plataforma: Arduino UNO
## Componentes Utilizados
- **Arduino Uno**

    Microcontrolador responsável por coordenar o movimento dos dois motores simultaneamente.
- **Módulo de Motor Ponte H dupla L298N**

    A partir da programação estabelecida no Arduino IDE, ele controla o movimento dos motores.
- **Chassi**

    O chassi servirá de suporte para o encaixe de todos os componentes necessários no projeto.

- **2 Motor DC 3-6V**

    Os motores serão responsáveis por fazer a roda girar sendo controlados pelo Módulo de Motor.

- **2 Rodas**

    As rodas dão suporte ao chassi facilitando seu transporte por terem formato circular. Os motores DC que as fazem girar.

- **Bateria 9V**

    Responsável por alimentar o Arduino Uno, já  que não estará conectado a nenhuma outra fonte externa.

- **Suporte para 4 Pilhas 1,5V**

    Servirão de fonte de alimentação para os dois motores.

- **1 Rodinha de Gel Giratória**

    Servirá de suporte para manter o chassi reto e em pé.

- **Fios de Conexão(jumpers)**

    Serão necessários para se fazer todas as conexões.

- **Módulo Sensor de Distância Ultrassônico HC-SR04**

    Esse sensor envia pulsos ultrassônicos e os recebe de volta, possibilitando a captura de dados de distância à um obstáculo em sua frente.

## Descrição
Este projeto implementa um robô de duas rodas, que através de  um medidor ultrassônico, o ajuda a não esbarrar em nenhuma estrutura que estiver em seu caminho. Isso tudo sem nenhum controle de fora, totalmente automático e de uso prático, sendo ideal para exposições de robótica.

### Funcionamento 
**1. Captação de Dados**

  **- Módulo Sensor de Distância Ultrassônico HC-SR04:** 
  
O sensor envia um pulso ultrassônico, a onda é bloquada por algum possível obstáculo e é retornada. O Arduino usa esse tempo de ida e volta, e com base na fórmula: *Distância  = (Tempo de duração do sinal de saída × velocidade do som) / 2)*, será possível saber a distância entre o medidor ultrassônico e um obstáculo à sua frente, pois como sabemos a velocidade do som(pulso ultrassônico) e o tempo de duração(ida e volta), posteriormente será possível calcular a distância.

  **- Ideia da Programação:** 
  
Agora que sabemos a distância, é só produzir um código em que quando a distância for menor que tal quantia, terá uma consequência, que por exemplo pode ser o robô ir para trás. E se a distância for maior, o robô fazerá o contrário que no caso será ir para frente. Essa é a ideia em que todo este projeto é baseada; ela possui várias aplicações e o usuário poderá usá-la da maneira que quiser, para construir, assim, o seu projeto.










