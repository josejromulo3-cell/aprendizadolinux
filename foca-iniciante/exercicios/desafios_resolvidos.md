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
