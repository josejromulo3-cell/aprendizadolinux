# 📁 Registro de Comandos - Módulo 2: Comandos Básicos

Este arquivo serve como meu diário técnico de comandos exercitados durante o estudo do Guia Foca Linux.

---

### `pwd`
* **Objetivo:** Exibir o caminho absoluto do diretório de trabalho atual.
* **Sintaxe:** `pwd [opções]`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~/Downloads/projetos linux/aprendizadolinux$ pwd
    ```
* **Saída Obtida:**
    ```text
    /home/romulo/Downloads/projetos linux/aprendizadolinux
    ```
* **Explicação da Saída:** Retornou o caminho completo da pasta onde meu repositório local está inicializado.
* **O que aprendi:** Essencial para localização espacial dentro da árvore do sistema de arquivos.

---

### `ls`
* **Objetivo:** Listar o conteúdo de um diretório.
* **Sintaxe:** `ls [opções] [diretório]`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ ls Documentos/
    ```
* **Saída Obtida:**
    ```text
    foca_linux.txt  projetos  ufpb
    ```
* **Explicação da Saída:** Exibiu os arquivos e subpastas existentes dentro do diretório especificado.
* **O que aprendi:** Por padrão, lista o diretório atual se nenhum caminho for passado.

---

### `ls -la`
* **Objetivo:** Listar todo o conteúdo detalhado, incluindo arquivos ocultos.
* **Sintaxe:** `ls -la [diretório]`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ ls -la
    ```
* **Saída Obtida:**
    ```text
    drwxr-xr-x  4 romulo romulo 4096 jun 17 10:00 .
    -rw-------  1 romulo romulo  512 jun 17 11:15 .bash_history
    drwxr-xr-x  2 romulo romulo 4096 jun 17 09:30 Documentos
    ```
* **Explicação da Saída:** Exibe permissões, donos, tamanho e arquivos ocultos (que começam com `.`).
* **O que aprendi:** A flag `-l` detalha os atributos e a `-a` mostra arquivos ocultos do sistema.

---

### `cd`
* **Objetivo:** Mudar o diretório de trabalho atual.
* **Sintaxe:** `cd [diretório]`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ cd /etc/apt
    ```
* **Explicação da Saída:** O prompt do terminal muda indicando a nova localização.
* **O que aprendi:** `cd ..` sobe um nível na árvore e `cd ~` volta para a pasta home.

---

### `mkdir`
* **Objetivo:** Criar diretórios.
* **Sintaxe:** `mkdir [opções] nome`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ mkdir -p ufpb/periodo_01
    ```
* **O que aprendi:** A flag `-p` cria os diretórios pais automaticamente se eles não existirem.

---

### `rmdir`
* **Objetivo:** Remover diretórios vazios.
* **Sintaxe:** `rmdir nome_do_diretorio`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ rmdir ufpb/periodo_01
    ```
* **O que aprendi:** Falha por segurança se o diretório tiver qualquer arquivo dentro.

---

### `cp`
* **Objetivo:** Copiar arquivos ou diretórios.
* **Sintaxe:** `cp [opções] origem destino`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ cp foca.txt ufpb/backup_foca.txt
    ```
* **O que aprendi:** Para copiar pastas inteiras com arquivos dentro, deve-se usar a flag recursiva `-r`.

---

### `mv`
* **Objetivo:** Mover ou renomear arquivos e diretórios.
* **Sintaxe:** `mv origem destino`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ mv foca.txt anotacoes_foca.txt
    ```
* **O que aprendi:** Mover e renomear utilizam a mesma ferramenta base no Linux.

---

### `rm`
* **Objetivo:** Remover arquivos ou diretórios.
* **Sintaxe:** `rm [opções] alvo`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ rm -rf ufpb/
    ```
* **O que aprendi:** Apaga permanentemente sem passar por lixeira. A flag `-rf` força a remoção de pastas completas.

---

### `cat`
* **Objetivo:** Exibir o conteúdo completo de um arquivo na tela.
* **Sintaxe:** `cat arquivo`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ cat /etc/hostname
    ```
* **Saída Obtida:**
    ```text
    Romulo
    ```
* **O que aprendi:** Excelente para arquivos pequenos, mas ruim para ler arquivos muito grandes.

---

### `less`
* **Objetivo:** Visualizar arquivos de texto de forma paginada e navegável.
* **Sintaxe:** `less arquivo`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ less /var/log/dpkg.log
    ```
* **O que aprendi:** Abre uma tela interativa. Usa as setas do teclado para navegar e a tecla `q` para sair.

---

### `grep`
* **Objetivo:** Filtrar linhas que contenham um termo específico em um arquivo.
* **Sintaxe:** `grep "termo" arquivo`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ grep "romulo" /etc/passwd
    ```
* **O que aprendi:** Um dos filtros mais poderosos do Linux para buscar dados em logs e configurações.

---

### `find`
* **Objetivo:** Buscar arquivos na árvore de diretórios com base em regras.
* **Sintaxe:** `find caminho criterios`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ find . -name "*.md"
    ```
* **O que aprendi:** Varre o disco em tempo real procurando padrões (como extensões de arquivo).

---

### `chmod`
* **Objetivo:** Alterar as permissões de leitura, escrita e execução de arquivos.
* **Sintaxe:** `chmod permissoes arquivo`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ chmod +x script.sh
    ```
* **O que aprendi:** Transforma arquivos de texto comuns em programas executáveis com a permissão `+x`.

---

### `chown`
* **Objetivo:** Alterar o proprietário e o grupo de um arquivo.
* **Sintaxe:** `chown dono:grupo arquivo`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ sudo chown root:root notas.txt
    ```
* **O que aprendi:** Apenas o superusuário (`root`) ou o uso do `sudo` pode mudar o dono de um arquivo.

---

### `ps`
* **Objetivo:** Exibir os processos ativos no sistema naquele instante.
* **Sintaxe:** `ps [opções]`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ ps aux
    ```
* **O que aprendi:** A combinação `aux` mostra processos de todos os usuários de forma detalhada.

---

### `top`
* **Objetivo:** Monitorar os processos em tempo real e o consumo de hardware.
* **Sintaxe:** `top`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ top
    ```
* **O que aprendi:** Funciona como o gerenciador de tarefas. Atualiza continuamente até que a tecla `q` seja pressionada.

---

### `kill`
* **Objetivo:** Enviar um sinal para encerrar um processo através do seu ID (PID).
* **Sintaxe:** `kill [sinal] PID`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ kill -9 1234
    ```
* **O que aprendi:** O sinal `-9` força a finalização imediata e abrupta de um processo travado.

---

### `tar`
* **Objetivo:** Empacotar e compactar arquivos (gerando arquivos .tar.gz).
* **Sintaxe:** `tar [opções] destino origens`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ tar -czvf backup.tar.gz Documentos/
    ```
* **O que aprendi:** `-c` cria o arquivo, `-z` comprime com gzip, `-v` lista o processo e `-f` define o nome do arquivo.

---

### `zip`
* **Objetivo:** Compactar arquivos no formato padrão .zip.
* **Sintaxe:** `zip [opções] destino origens`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ zip -r estudos.zip foca-iniciante/
    ```
* **O que aprendi:** A flag `-r` é obrigatória para incluir pastas e subpastas de forma recursiva.

---

### `unzip`
* **Objetivo:** Extrair arquivos compactados no formato .zip.
* **Sintaxe:** `unzip arquivo.zip`
* **Comando Utilizado:**
    ```bash
    romulo@Romulo:~$ unzip estudos.zip -d /home/romulo/Downloads/
    ```
* **O que aprendi:** A flag `-d` permite escolher o diretório exato de destino para onde os arquivos extraídos irão.
