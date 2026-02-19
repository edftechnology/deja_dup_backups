# Como configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using the `Déjà Dup Backups` on `Linux Ubuntu`._

## Descrição [2]

### `Déjà Dup Backups`

O Déjà Dup Backups é uma ferramenta de backup simples e intuitiva para sistemas baseados em Linux, como o Ubuntu. Ele oferece uma interface amigável para configurar e automatizar backups de arquivos e diretórios importantes. Com o Déjà Dup, os usuários podem programar backups regulares para dispositivos locais, como discos rígidos externos, ou serviços de armazenamento em nuvem, como o Google Drive ou o Dropbox. Além disso, ele suporta criptografia para proteger os dados sensíveis durante o armazenamento e oferece opções de restauração fáceis para recuperar arquivos em caso de perda ou falha do sistema. É uma solução eficaz e confiável para manter os dados seguros e acessíveis.


## 1. Como configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o terminal. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes APT. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo APT e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    2.5 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.6 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    2.7 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.8 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

Para configurar/instalar o `Déjà Dup Backups`, um aplicativo de _backup_ muito utilizado no `Linux Ubuntu`, através do `Terminal Emulator`, você pode seguir os seguintes passos. Este processo geralmente envolve a utilização de comandos `apt` para instalar pacotes de _software_ no `Linux Ubuntu` e em outras distribuições baseadas em `Debian`.

3. **Instale o `Déjà Dup`:** Após atualizar a lista de pacotes, instale o `Déjà Dup` com o comando:

    ```
    sudo apt install deja-dup -y
    ```

    Esse comando irá baixar e instalar o `Déjà Dup` e todas as dependências necessárias. Durante a instalação, pode ser que o sistema peça a confirmação para continuar, para isso, você deve pressionar `Y` e então `Enter`.

4. **Verifique a Instalação:** Após a instalação, você pode verificar se o `Déjà Dup` foi instalado corretamente digitando `deja-dup` no `Terminal Emulator` ou procurando por ele no menu de aplicativos.

5. **Use o `Déjà Dup`:** Agora que o `Déjà Dup` está instalado, você pode configurá-lo e começar a fazer _backups_ dos seus arquivos. Ele oferece uma interface gráfica intuitiva, facilitando o processo de _backup_ e restauração.


O `Déjà Dup Backups` é projetado para ser uma ferramenta de backup que respeita a privacidade do usuário e a segurança dos dados. Aqui estão alguns pontos importantes que garantem que ele não "puxe" ou colete seus dados de maneira indevida:

1. **Controle do Usuário:** O `Déjà Dup` dá ao usuário total controle sobre o que é copiado e para onde. O usuário especifica os diretórios de origem para _backup_ e o destino onde os _backups_ serão armazenados. Isso pode ser um dispositivo de armazenamento local, um _drive_ externo, ou uma conta de armazenamento em nuvem escolhida pelo usuário.

2. **Privacidade e Segurança:** Por padrão, o `Déjà Dup` realiza _backups_ criptografados, o que significa que seus dados são protegidos e não podem ser lidos por outros sem a chave de criptografia. Isso é particularmente importante quando se está usando armazenamento em nuvem como destino de _backup_.

3. **_Software_ Livre:** O `Déjà Dup` é _software_ livre, o que significa que seu código-fonte é aberto e disponível para revisão. Isso permite que a comunidade examine o _software_ em busca de potenciais vulnerabilidades de segurança ou comportamentos maliciosos, como a coleta não autorizada de dados.

4. **Sem Coleta de Dados:** Não há mecanismos dentro do `Déjà Dup` que coletam ou enviam seus dados pessoais para servidores externos (com exceção do destino de _backup_ escolhido por você, como um serviço de nuvem, onde os dados são enviados para serem armazenados). O propósito do _software_ é puramente realizar _backups_ e restaurações conforme configurado pelo usuário.

5. **Transparência:** Sendo um projeto de código aberto, as atualizações e as mudanças no `Déjà Dup` são documentadas e disponíveis para o público. Isso garante uma camada adicional de transparência em relação a como o _software_ opera e é desenvolvido.

É importante, no entanto, praticar uma vigilância contínua em relação a qualquer _software_ que você use, especialmente quando ele lida com dados pessoais ou sensíveis. Certificar-se de que você está usando a versão mais recente do `Déjà Dup` e que seu destino de _backup_ é seguro e confiável também são práticas recomendadas para manter seus dados seguros.


### 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `Déjà Dup Backups` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean
    sudo apt autoclean -y
    sudo apt autoremove -y
    sudo apt update -y
    sudo apt autoremove -y
    sudo apt autoclean -y
    sudo apt install deja-dup -y
    ```


## 2. Desinstalar o `Déjà Dup Backups` do `Linux Ubuntu`

Para desinstalar o `Déjà Dup Backups` do seu sistema `Linux Ubuntu` pelo `Terminal Emulator`, você pode seguir os passos abaixo. A desinstalação remove o programa do seu sistema, mas geralmente mantém as configurações e os arquivos de _backup_, a menos que você opte por removê-los manualmente.

1. **Abra o `Terminal Emulator`**: Você pode acessar o `Terminal Emulator` pressionando `Ctrl+Alt+T` ou procurando por `Terminal` no menu de aplicativos.

2. **Desinstale o `Déjà Dup`**: Utilize o comando `apt` para remover o pacote. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt remove deja-dup -y
    ```

    Este comando remove o aplicativo do seu sistema.

3. **Remova Dependências Não Utilizadas**: Após desinstalar o `Déjà Dup`, pode ser uma boa prática remover as dependências que foram instaladas com o aplicativo e que não são mais necessárias. Você pode fazer isso com o comando:

    ```
    sudo apt autoremove -y
    ```

    Esse comando limpa os pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários.

4. **Limpe o _Cache_ de Pacotes**: Após a remoção, você pode querer limpar o _cache_ de pacotes baixados para liberar espaço no disco. Isso é feito com o comando:

    ```
    sudo apt clean
    ```

    Este comando remove arquivos de pacotes (.deb) armazenados em cache que foram baixados durante a instalação de pacotes.


### 2.1 Removendo Configurações e Dados de _Backup_

Se você deseja também remover as configurações pessoais e possíveis dados de _backup_ gerenciados pelo `Déjà Dup`, será necessário localizar e excluir esses arquivos manualmente. Eles geralmente estão localizados em diretórios ocultos na pasta home do usuário, por exemplo:

* **Configurações do `Déjà Dup`**: `~/.config/deja-dup/`

* Arquivos de _backup_ locais (dependendo de onde você configurou para salvá-los)

Para remover essas configurações, você pode usar:

```
rm -r ~/.config/deja-dup/
```

**Nota**: Tenha cuidado ao usar comandos de remoção, especialmente ao lidar com _backups_. Certifique-se de que não precisa mais dos dados ou tenha uma cópia em outro lugar antes de excluí-los definitivamente.

## Referências

[1] OPENAI. ***Instale déjà dup via terminal.*** Disponível em: <https://chat.openai.com/c/d89b8216-2d5a-4300-a2db-dd075d12827d> (texto adaptado). Acessado em: 03/04/2023 17:11.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 03/04/2024 17:10.

