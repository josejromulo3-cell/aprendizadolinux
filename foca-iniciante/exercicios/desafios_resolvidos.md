# 🏆 Resolução dos Desafios Técnicos - Foca Linux

Este arquivo documenta a resolução dos desafios práticos propostos para testar meus conhecimentos em manipulação de arquivos, filtros de texto e permissões.

---

## Desafio 1: O Inspetor de Arquivos
- **Objetivo:** Filtrar linhas específicas em um arquivo de texto.
- **Comandos Utilizados:**
  ```bash
  mkdir desafio_busca
  nano historia.txt
  grep "Linus" historia.txt

O que aprendi: O comando grep é uma ferramenta indispensável para buscar padrões de texto e analisar arquivos de log sem precisar abri-los por completo.

Desafio 2: O Organizador de Bagunça

    Objetivo: Criar, mover, copiar e renomear arquivos.

    Comandos Utilizados:
touch foto1.png foto2.png texto.txt
mkdir imagens
mv foto1.png foto2.png imagens/
cp texto.txt imagens/copia_segura.txt

O que aprendi: Compreendi como o comando mv gerencia tanto a movimentação quanto a renomeação de arquivos, e como o cp realiza cópias estruturadas para outros diretórios.

Desafio 3: O Administrador de Sistemas

    Objetivo: Analisar e modificar permissões de arquivos no Linux.

    Comandos Utilizados:

touch backup_ufpb.sh
ls -l backup_ufpb.sh
chmod +x backup_ufpb.sh

O que aprendi: Entendi que por padrão os arquivos nascem sem permissão de execução por segurança. A flag +x com o comando chmod ativa o bit de execução, transformando o arquivo em um script executável.


---

## Desafio 4: O Caçador de Processos
- **Objetivo:** Localizar e finalizar processos em segundo plano.
- **Comandos Utilizados:**
  ```bash
  sleep 1000 &
  ps aux | grep sleep
  kill -9 14064

O que aprendi: Aprendi a identificar o PID (Process ID) na tabela do ps aux e descobri que o comando kill -9 força o encerramento imediato do processo selecionado.


Desafio 5: O Analista de Logs

    Objetivo: Visualizar e analisar arquivos de log do sistema.

    Comandos Utilizados:
less /var/log/dpkg.log
tail /var/log/dpkg.log

O que aprendi: O comando less permite navegar de forma paginada por arquivos grandes usando as setas do teclado (saindo com 'q'). Já o comando tail é ideal para checar rapidamente as últimas 10 linhas de um log em tempo real.


Desafio 6: O Especialista em Backup

    Objetivo: Instalar ferramentas e gerenciar arquivos compactados.

    Comandos Utilizados:

sudo apt update && sudo apt install -y zip unzip
zip -r backup_estudos.zip "projetos linux"/aprendizadolinux
mkdir teste_extracao
mv backup_estudos.zip teste_extracao/
cd teste_extracao
unzip backup_estudos.zip

O que aprendi: Compreendi como instalar pacotes no Debian usando o apt. Aprendi a importância da flag -r no comando zip para incluir subpastas recursivamente e como o unzip extrai os arquivos de volta.
