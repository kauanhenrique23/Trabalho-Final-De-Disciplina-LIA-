# Sinalizador de Garagem
# Descrição
Este projeto visa criar um sinalizador de garagem através de dois LED's e uma programação básica. A partir desta ideia pode-se ir muito além da imaginação e desenvolver diversos projetos com diversas utilidades.
# Funcionamento
- **LED_1 aceso:** Quando o LED_1 estiver aceso, pode-se já concluir que o LED_2 estará apagado.
- **LED_2 aceso:** Quando o LED_2 estiver aceso, pode-se já concluir que o LED_1 estará apagado.
- **Ordem de Ligação:** Primeiramente se acenderá o LED_1, e depois de 1 segundo ele irá se apagar e o LED_2 se acenderá. E quando o LED_2 se apagar o ciclo será reiniciado.
# Materiais Necessários
- **1 Arduino UNO**
- **1 Protoboard**
- **2 Led's (de preferência de cores diferentes)**
- **2 Resistores 10KΩ**
- **Fios de Conexão (jumpers)**
# Montagem do Circuito
**1. Ligação dos LED's**

- Ligue o GND (0V) da placa do Arduino ao GND da fileira vertical do Protoboard.
- Coloque os dois LED's no Protoboard de modo que os dois terminais fiquem dispostos em fileiras diferentes. E de preferência coloque-os alinhados verticalmente.
- Com fios jumpers conecte o GND do Protoboard ao ânodo (terminal menor) dos LED's.
- Ligue, através de fios jumpers e passando por resistores, os pinos digitais 2 e 3 respectivamente ao cátodo (terminal maior) dos LED_1 e LED_2.
