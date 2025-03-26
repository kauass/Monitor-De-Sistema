# Monitoramento de Sistema em Node.js

Este projeto é um monitoramento de sistema desenvolvido em Node.js que captura e exibe informações do sistema operacional, como tempo de atividade, uso de memória RAM e detalhes do processador. Além disso, ele salva logs dessas informações em um arquivo de texto.

## Tecnologias Utilizadas

O projeto utiliza os seguintes módulos nativos do Node.js:
- `os`: Para obter informações sobre o sistema operacional.
- `fs`: Para manipulação de arquivos e diretórios.
- `path`: Para manipulação de caminhos de arquivos.

## Funcionamento

O código realiza as seguintes operações a cada segundo:
1. Captura informações do sistema usando o módulo `os`.
2. Exibe os detalhes no console.
3. Salva os logs dessas informações em um arquivo `log.txt` dentro de um diretório `log`.

## Estrutura do Código

### `getSystemInfo()`
Esta função coleta os seguintes dados do sistema:
- **Sistema Operacional** (Windows, Linux, MacOS, FreeBSD)
- **Arquitetura do Processador**
- **Modelo do Processador**
- **Tempo de Atividade do Sistema**
- **Uso Total e Percentual da Memória RAM**

### `printLog(info)`
Exibe no console as informações do sistema formatadas.

### `saveLog(info)`
Salva as informações capturadas em um arquivo `log.txt`, dentro de um diretório `log`. Caso o diretório não exista, ele é criado automaticamente.

### `setInterval()`
Executa a coleta, exibição e salvamento das informações a cada segundo.

## Como Executar

1. Certifique-se de ter o Node.js instalado em seu sistema.
2. Salve o código em um arquivo, por exemplo, `monitor.js`.
3. No terminal, execute:
   ```sh
   node monitor.js
   ```
4. As informações do sistema serão exibidas no console e armazenadas no arquivo `log.txt`.

## Observações
- O código limpa o console a cada atualização para exibir apenas as informações mais recentes.
- O diretório `log` é criado automaticamente, caso não exista.
- O log é atualizado continuamente, sem sobrescrever os dados anteriores.
