# Como configurar/instalar/usar o `configurar impressora` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `configurar impressora` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using the `configurar impressora` on `Linux Ubuntu`._


## Descrição [2]

### `configurar impressora`

Print produce (books, newspapers, magazines, etc.), especially in large quantities, by a mechanical process involving the transfer of text, images, or designs to paper.
"a thousand copies of the book were printed"


## 1. Como configurar/instalar/usar o `configurar impressora` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `configurar impressora` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

### 1.1 Usar Ferramentas Gráficas

Se preferir, pode usar ferramentas gráficas para descobrir impressoras de rede. Algumas delas incluem:

#### 1.1.1 Ferramenta de Configuração de Impressoras do Sistema

1. No ambiente de desktop GNOME, vá para `"Configurações"` -> `"Impressoras"` e clique em `"Adicionar Impressora"`.

2. O sistema irá procurar automaticamente por impressoras de rede.

#### 1.1.2 Ferramenta `system-config-printer`

1. Abra um `Terminal Emulator` e instale a ferramenta (se necessário): `sudo apt install system-config-printer -y`

2. Execute a ferramenta: `system-config-printer`

3. Clique em `"Adicionar"` para procurar e configurar impressoras de rede.

### 2. Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `configurar impressora` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    NÃO há.
    ```


## Referências

[1] OPENAI. ***Descobrindo Impressoras na Rede.*** Disponível em: <https://chatgpt.com/c/0a6e15e1-7860-4c61-80a6-eaf916a59ae1> (texto adaptado). Acessado em: 22/05/2024 12:27.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 22/05/2024 12:27.

