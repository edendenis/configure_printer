# Como configurar/instalar/usar o `alterar as permissões de pastas e arquivos` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `alterar as permissões de pastas e arquivos` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using the `alterar as permissões de pastas e arquivos` on `Linux Ubuntu`._


## Revisão(ões)/Versão(ões)

| Revisão número | Data da revisão | Descrição da revisão                                    | Autor da revisão                                |
|:--------------:|:---------------:|:--------------------------------------------------------|:------------------------------------------------|
| 0              | 30/04/2024      | <ul><li>Revisão inicial/criação do documento.</li></ul> | <ul><li>Eden Denis F. da S. L. Santos</li></ul> |


## Descrição [2]

### `alterar as permissões de pastas e arquivos`

No Linux Ubuntu, as permissões de pastas e arquivos são atributos que determinam quais usuários ou grupos podem acessar, modificar ou executar esses recursos. Cada arquivo e pasta possui permissões específicas para o proprietário, o grupo associado e outros usuários. As permissões são representadas por letras e números, indicando diferentes níveis de acesso, como leitura (r), escrita (w) e execução (x). O comando chmod é usado para modificar as permissões, enquanto chown é usado para alterar o proprietário e o grupo de um arquivo ou pasta. Essas permissões são fundamentais para garantir a segurança e a integridade do sistema operacional.

## 1. Como configurar/instalar/usar o `alterar as permissões de pastas e arquivos` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `alterar as permissões de pastas e arquivos` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes APT. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo APT e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    2.5 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.6 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    2.7 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.8 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

### 1.1 Conceder permissões com notação simbólica

No `Linux Ubuntu`, você pode alterar as permissões de uma pasta usando o comando `chmod`. Este comando permite que você especifique diferentes níveis de permissão para o proprietário do arquivo, para o grupo ao qual o arquivo pertence e para outros usuários.

Aqui está a estrutura básica do comando: `chmod [opções] [modo] [arquivo ou diretório]`

- **`[opções]`**: Modificadores adicionais para o comando. Por exemplo, `-R` para aplicar recursivamente a diretórios e seus conteúdos.

- **`[modo]`**: Pode ser especificado de algumas formas, como por número (por exemplo, `755`) ou por notação simbólica (por exemplo, `u+rwx`, `g+rx`, `o+rx`), onde `u` é o usuário (proprietário), `g` é o grupo e o são outros.

- **`[arquivo ou diretório]`**: O caminho para o diretório ou arquivo cujas permissões você deseja alterar.

1. Por exemplo, se você quiser que o proprietário tenha todas as permissões (ler, escrever, executar), o grupo tenha permissões de leitura e execução e outros usuários tenham apenas permissão de leitura para uma pasta chamada `minhapasta`, você pode usar: `chmod 754 minhapasta`

2. Ou, usando a notação simbólica: `chmod u+rwx,g+rx,o+r minhapasta`

3. Se precisar aplicar a mudança recursivamente a todos os arquivos e subdiretórios dentro de `minhapasta`, você adicionaria o `-R`: `chmod -R 754 minhapasta`

### 1.2 Conceder notações pelo usuário e gruo por nome

Se você deseja especificar o usuário e o grupo por nome, ao invés de usar a notação simbólica para permissões, você provavelmente está falando sobre o comando `chown`, que é usado para mudar a propriedade de um arquivo ou diretório.

O comando `chown` permite que você altere o proprietário e/ou o grupo de um arquivo ou diretório. A sintaxe básica é: `chown [opções] [usuário][:grupo] [arquivo ou diretório]`

- **`[usuário]`**: Nome do novo proprietário do arquivo.

- **`[:grupo]`**: Nome do novo grupo do arquivo. Este é opcional; se você omitir o grupo, apenas o proprietário será alterado.

- **`[arquivo ou diretório]`**: O caminho para o diretório ou arquivo cujo proprietário ou grupo você deseja alterar.

1. **Exemplo**

1.1 Suponha que você queira mudar a propriedade do diretório `minhapasta` para o usuário `edenedfsls` e o grupo `edenedfsls`. Você pode usar o comando: `chown edenedfsls:edenedfsls minhapasta`

1.2 Este comando atribuirá tanto a propriedade do usuário quanto a do grupo para `edenedfsls`. Se quiser aplicar essa mudança recursivamente a todos os arquivos e subdiretórios dentro de `minhapasta`, você adicionaria a opção `-R`: `chown -R edenedfsls:edenedfsls minhapasta`

    Isso garantirá que todos os arquivos e subdiretórios dentro de `minhapasta` sejam atualizados para ter `edenedfsls` como seu proprietário e grupo.

### 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `alterar as permissões de pastas e arquivos` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o terminal. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    NÃO há.
    ```


## Referências

[1] OPENAI. ***Alterar Permissões da Pasta*** Disponível em: <https://chat.openai.com/c/cf51c1c3-bb9d-4b12-94a0-eb25db5f4882> (texto adaptado). Acessado em: 30/04/2023 17:11.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 30/04/2024 17:10.

