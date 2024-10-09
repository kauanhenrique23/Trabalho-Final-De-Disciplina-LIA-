# Sequencial de 3 Canais
# Descrição
Este projeto visa criar uma sincronia entre três LED's ao caso que acendam em ordem e harmonicamente. Usando esta ideia será possui produzir inúmeros tipos de mecanismos que utilizamos em nosso cotidiano, como por exemplo, um sinalizador de garagem ou até mesmo um semáforo.
# Funcionamento
- **LED_1 aceso:** Quando o LED_1 estiver aceso o resto dos LED's estarão apagados. Se o LED_1 não estiver aceso significa que algum dos outros dois LED's estão aceso.
- **LED_2 aceso:** Quando o LED_2 estiver aceso o resto dos LED's estarão apagados. Se o LED_2 não estiver aceso significa que algum dos outros dois LED's estão aceso.
- **LED_3 aceso:** Quando o LED_3 estiver aceso o resto dos LED's estarão apagados. Se o LED_3 não estiver aceso significa que algum dos outros dois LED's estão aceso.
- **Ordem de Ligação:** Primeiramente se acenderá o LED_1, em seguida ele se apagará e ao mesmo tempo o LED_2 acenderá, logo depois, o LED_2 se apagará e o LED_3 acenderá. E então, quando o LED_3 se apagar o ciclo será reiniciado.
- 
# Materiais Necessários
- 1 Arduino UNO
- 1 Protoboard
- 3 LED's (preferencialmente de colorações diferentes)
- 3 Resistores 10KΩ
- Fios de Conexão (jumpers)

# Montagem do Circuito
**1. Ligação dos LED's**

- Através de cabos jumpers ligue o GND (0V) da placa do Arduino ao GND do Protoboard.
- No Protoboard coloque os 3 LED's alinhados em si numa mesma linha vertical (lembre-se de colocar o ânodo e o cátodo dos LED's em fileiras horizontais diferentes).
- Ligue, através de fios jumpers, o GND da placa do Arduino UNO ao ânodo (terminal menor) de cada LED.
- Com os resistores e alguns fios jumpers ligue o cátodo (terminal maior) dos LED's aos pinos digitais 2, 3, 4 da placa do Arduino UNO, respectivamente à ordem de posição dos LED's.
