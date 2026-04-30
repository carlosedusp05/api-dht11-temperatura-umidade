# monitoramento-clima-api
## Dashboard de Temperatura e Umidade com ESP32 e Integração API - Projeto Didático IIoT

Este projeto foi desenvolvido como parte das atividades práticas do curso de **IIoT (Internet das Coisas Industrial)** no **SENAI**. O objetivo principal é coletar dados ambientais de temperatura e umidade em tempo real utilizando um ESP32 e transmiti-los para uma API REST personalizada, permitindo o armazenamento e a consulta histórica das medições.

## Descrição do Projeto

O sistema utiliza um sensor **DHT11** acoplado ao **ESP32** para realizar a leitura das variáveis climáticas. O microcontrolador conecta-se à rede Wi-Fi e envia os dados via requisições HTTP para uma API desenvolvida em Node.js e hospedada no **Render**. 

Esta aplicação simula cenários industriais reais onde o monitoramento de condições ambientais é crítico, como em servidores (data centers), estoques de insumos sensíveis ou estufas automatizadas, onde os dados precisam ser centralizados para análise futura.

## Recursos e Componentes

Para a montagem deste esquema, foram utilizados os seguintes itens:

* **Microcontrolador:** ESP32
* **Sensor:** DHT11 (Temperatura e Umidade)
* **Conexão:** Protoboard e Jumpers (Macho-Fêmea / Macho-Macho)
* **Alimentação/Dados:** Cabo Micro-USB
* **Plataforma Cloud (API):** Render
* **Protocolo de Comunicação:** HTTP / REST

## Endpoints da API

A API está disponível no seguinte endereço:
* **URL de Consulta:** `https://api-dht11-temperatura-umidade.onrender.com/dados`

### Exemplo de Resposta (JSON)
Ao acessar o endpoint de dados, a API retorna o histórico das medições no seguinte formato:
```json
[
  {
    "temperatutra": "22.60",
    "umidade": "69.00",
    "data": "2026-04-30T19:18:22.756Z"
  }
]