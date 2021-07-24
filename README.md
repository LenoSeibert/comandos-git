<h1>Manual do Git</h1>
<h2>00 - Configurações Iniciais</h2>
<pre>
      <code>
<strong color="red">sudo apt install git<strong> #instala o git no linux/debian e distros baseadas
      git config --global user.name &quot;Seu Nome&quot; #Define identidade-Nome de usuário do GITHUB
      git config --global user.email &quot;Seu Email&quot; #Define identidade - Email do GITHUB
      #Isso marca o histórico com seu ID
      </code>
  </pre>
<h2>02 - Ver todas as opções de configuração</h2>
<pre>
      <code>
      man git #mostra o manual do git
      git help #Mostra a pagina de ajuda do git 
      git help comando #para acessar a ajuda de um comando em especifico
      #Exemplo
      git help clone #Abre o manual do comando especifico.
      </code>
  </pre>
<h2>03 - Editor padrão</h2>
<pre>
    <code>
      git config --global core.editor &quot;code -w&quot; #Substitui o editor padrão VIM pelo VSCODE
    </code>
  </pre>
<h2>04 - Ver quais configurações estão definidas</h2>
<pre>
    <code>
      git config --list #mostra as configurações atuais
    </code>
  </pre>
<h2>05 - Ativar color.ui </h2>
<p>
  Deixa o terminal mais amigável, marcando com cores, as ações
  tomadas
</p>
<pre>
  <code>
    git config --global color.ui true 
  </code>
</pre>
<h2>06 - Para criar um repositório em um projeto.</h2>
<pre>
  <code>#Na pasta do projeto
git init #Inicia um repositorio e cria uma pasta .git com as configuraçoes do projeto
ls -a #para ver se a pasta oculta foi criada
</code>
</pre>
<p>
  <strong>ATENÇÃO</strong>
  Todo o Histórico da versão e arquivos de configuração ficam dentro da pasta <strong>.git </strong>
  Apagar a pasta <strong>.git</strong> vai ocasionar a perda de todo o histórico.
</p>
<h2>07 - Fazer Commit</h2>
<pre>
  <code>git add . #Prepara todos os arquivos da pasta para um ponto na História
git add nomeDoArquivo #Prepara um arquivo especifico para adicionar
git commit -m &quot;Commit Inicial&quot; #Cria o ponto na História
#o -m é para definir um comentario
</code>
</pre>
<h2>08 - Mostrar Histórico de mudanças</h2>
<pre>
  <code>git log #Mostra um Historico dos pontos na História
git log --oneline #Histórico resumido
git log -n 5 #Traz os ultimos 5 commits
git log --grep=&quot;palavra chave&quot; #Busca por palavra chave
</code>
</pre>
<h2>09 - Os 3 estados </h2>
<pre>
  <code>git init #Inicia um repositorio - Working Directory
git add . #Prepara todos os arquivos - Stage Area
git commit -m &quot;Commit Inicial&quot; #Cria o ponto na História Local 
</code>
</pre>
<h2>10 - Ignorando arquivos e Diretórios</h2>
<pre>
  <code>
    touch .gitignore #Cria arquivo git ignore
nano .gitignore #Abre o arquivo para edição
#Para ignorar arquivos ou pastas basta adicionar seu nome no arquivo
git add .gitignore
</code>
</pre>
<h2>11 - Situação atual</h2>
<pre>
  <code>
    git status # Este comando mostra o estus atual 
  </code>
</pre>
<h2>12 - Remover arquivos adicionados</h2>
<pre>
  <code>
    git rm --cached nomeDoArquivo #Remove arquivos da Stage area
  </code>
</pre>
<h2>13 - Adicionar por extensão</h2>
<pre>
  <code>
    git add *.jsx # adicionar todos os arquivos com a extenção .js .php .html .ts etc..
</code>
</pre>
<h2>14 - Ver as alterações dos nos arquivos</h2>
<pre>
  <code>
    git diff #mostra o que foi alterado
  </code>
</pre>
<h2>15 - Renomeando arquivo</h2>
<pre>
  <code>
    git mv nome.txt nomeNovo.txt #Renomear arquivo
  </code>
</pre>
<h2>16 - Movendo arquivo</h2>
<pre>
  <code>
    git mv arquivo.txt pasta/arquivo.txt #Move arquivo
  </code>
</pre>
<h2>17 - Restaurando um arquivo</h2>
<pre>
  <code>
    git restore arquivo.txt #restaura arquivo do Working Directory
  </code>
</pre>
<h2>18 - Retirando arquivo do staged</h2>
<pre>
  <code>
    git restore --staged arquivo.txt #Remove arquivo do staged. 
git restore --staged . #Remove tudo do staged
#Bom pra quando é adicionado arquivos que não devem ser commitados 
</code>
</pre>
<h2>19 - Corrigindo o Commit anterior</h2>
<pre>
  <code>
    git commit --amend -m &quot;Mensagem&quot; #Corige o ultimo commit 
#OBS: Mais correto criar novo ponto na história
#então usar so quando adiciona um arquivo 
#Que não pode ficar na historia. 
#Como arquivo com dados sensiveis ou inuteis fora do escopo do projeto
</code>
</pre>
<h2>20 - Restaurando arquivo</h2>
<pre>
  <code>
    git checkout hash -- nomeDoArquivo #O hash marca de qual commit vai restaurar o arquivo
  </code>
</pre>
<h2>21 - Restaurando tudo</h2>
<pre>
  <code>
git revert HEAD~5 #O 5 são o numero de commits anteriores
#isso cria um nomo commit
git revert hash #mesmo resultado do anterior.
</code>
</pre>