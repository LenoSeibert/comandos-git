# Manual do Git

## 00 - Configurações Iniciais

```bash

sudo apt install git #instala o git no linux/debian e distros baseadas
git config --global user.name "Seu Nome" #Define identidade-Nome de usuário do GITHUB
git config --global user.email "Seu Email" #Define identidade - Email do GITHUB
#Isso marca o histórico com seu ID
```

## 02 - Ver todas as opções de configuração

```bash
man git #mostra o manual do git
git help #Mostra a pagina de ajuda do git 
git help comando #para acessar a ajuda de um comando em especifico
#Exemplo
git help clone #Abre o manual do comando especifico.
```

## 03 - Editor padrão

 

```bash
git config --global core.editor "code -w" #Substitui o editor padrão VIM pelo VSCODE
```

## 04 - Ver quais configurações estão definidas

```bash
git config --list #mostra as configurações atuais
```

## 05 - Ativar color.ui

Deixa o terminal mais amigável, marcando com cores, as ações tomadas

```bash
git config --global color.ui true 
```

## 06 - Para criar um repositório em um projeto.

```bash
#Na pasta do projeto
git init #Inicia um repositório e cria uma pasta .git com as configurações do projeto
ls -a #para ver se a pasta oculta foi criada
```

**ATENÇÃO**
Todo o Histórico da versão e arquivos de configuração ficam dentro da pasta **.git** 
Apagar a pasta **.git** vai ocasionar a perda de todo o histórico.

## 07 - Fazer Commit

```bash
git add . #Prepara todos os arquivos da pasta para um ponto na História
git add nomeDoArquivo #Prepara um arquivo especifico para adicionar
git commit -m "Commit Inicial" #Cria o ponto na História
#o -m é para definir um comentário

```

## 08 - Mostrar Histórico de mudanças

```bash
git log #Mostra um Histórico dos pontos na História
git log --oneline #Histórico resumido
git log -n 5 #Traz os últimos 5 commits
git log --grep="palavra chave" #Busca por palavra chave
```

## 09 - Os 3 estados

```bash
git init #Inicia um repositório - Working Directory
git add . #Prepara todos os arquivos - Stage Area
git commit -m "Commit Inicial" #Cria o ponto na História Local
```

## 10 - Ignorando arquivos e Diretórios

```bash
touch .gitignore #Cria arquivo git ignore
nano .gitignore #Abre o arquivo para edição
#Para ignorar arquivos ou pastas basta adicionar seu nome no arquivo
git add .gitignore
```

## 11 - Situação atual

```bash
git status # Este comando mostra o status atual 
```

## 12 - Remover arquivos adicionados

```bash
git rm --cached nomeDoArquivo #Remove arquivos da Stage area
```

## 13 - Adicionar por extensão

```bash
git add *.jsx # adicionar todos os arquivos com a extensão .js .php .html .ts etc..
```

## 14 - Ver as alterações dos nos arquivos

```bash
git diff #mostra o que foi alterado
```

## 15 - Renomeando arquivo

```bash
git mv nome.txt nomeNovo.txt #Renomear arquivo
```

## 16 - Movendo arquivo

```bash
git mv arquivo.txt pasta/arquivo.txt #Move arquivo
```

## 17 - Restaurando um arquivo

```bash
git restore arquivo.txt #restaura arquivo do Working Directory
```

## 18 - Retirando arquivo do staged

```bash
git restore --staged arquivo.txt #Remove arquivo do staged. 
git restore --staged . #Remove tudo do staged
```

## 19 - Corrigindo o Commit anterior

```bash
git commit --amend -m "Mensagem" #Corrige o ultimo commit 
#OBS: Mais correto criar novo ponto na história
#então usar so quando adiciona um arquivo 
#Que não pode ficar na historia. 
#Como arquivo com dados sensíveis ou inúteis fora do escopo do projeto
```

## 20 - Restaurando arquivo

```bash
git checkout hash -- nomeDoArquivo #O hash marca de qual commit vai restaurar o arquivo
```

## 21 - Restaurando tudo

```bash
git revert HEAD~5 #O 5 são o numero de commits anteriores
#isso cria um nomo commit
git revert hash #mesmo resultado do anterior.
```