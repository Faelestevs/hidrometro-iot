# Dispositivo IoT para monitoramento de consumo de água em tempo real

## Do que se trata o projeto?
O projeto se trata da utilização de um dispositivo de IoT para a solução de um problema recorrente no contexto atual, o consumo consciente dos recursos hídricos. Esses recursos estão se tornando cada vez mais escassos, e o intuito de nosso projeto é ajudar as pessoas a terem uma visão em tempo real do quanto o seu consumo impacta o meio ambiente e o seu bolso.

## Como foi construído?
O dispositivo de coleta de dados envolve a utilização de um Arduino, uma protoboard, um sensor de fluxo de água e jumpers para conectá-los. Esses elementos trabalham em conjunto para que os dados possam ser coletados de maneira confiável e enviados para a geração de relatórios ao usuário via API do Telegram e gráficos interativos no Grafana.

<img width="1920" height="944" alt="print-grafana" src="https://github.com/user-attachments/assets/dcf0ed13-69db-4a81-9b0a-1db6291fd910" />

O dashboard acima são exemplos de resultados que podem ser obtidos com o emprego da solução para monitor o consumo de água. Pode-se a presença de dados relevantes como o valor e o consumo médio nas contas de água, consumo em tempo real medido em litros por segundo e um histórico de faturas dos últmimos meses.

## Regra de negócios - Node-Red

<img width="1919" height="945" alt="node-red-print" src="https://github.com/user-attachments/assets/2ae91d03-64c7-40ad-8123-ead41a5f3217" />

Para que os Dashboards do Grafana chegassem naquele resultado, primeiro foi necessário que os dados crus obtidos pelo Arduino fossem tratados para se tornarem dados relevantes e legíveis. Cada fluxo cumpre um papel fundamental para o funcionamento da solução que envolve o cálculo de conta de água, conversões de medidas, comunicação com tópico do Broker via MQTT, formatação de mensagens, construção de objetos JSON, armazenamento e persistência no banco de dados, envio e recebimento de mensagens no Telegram.

## Link do vídeo
https://youtu.be/GSMC89hT29s
