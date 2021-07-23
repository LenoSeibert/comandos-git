# comandos-git
<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>Manual do Git</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	text-indent: -1.7em;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
}
.highlight-gray {
	color: rgb(155,154,151);
}
.highlight-brown {
	color: rgb(100,71,58);
}
.highlight-orange {
	color: rgb(217,115,13);
}
.highlight-yellow {
	color: rgb(223,171,1);
}
.highlight-teal {
	color: rgb(15,123,108);
}
.highlight-blue {
	color: rgb(11,110,153);
}
.highlight-purple {
	color: rgb(105,64,165);
}
.highlight-pink {
	color: rgb(173,26,114);
}
.highlight-red {
	color: rgb(224,62,62);
}
.highlight-gray_background {
	background: rgb(235,236,237);
}
.highlight-brown_background {
	background: rgb(233,229,227);
}
.highlight-orange_background {
	background: rgb(250,235,221);
}
.highlight-yellow_background {
	background: rgb(251,243,219);
}
.highlight-teal_background {
	background: rgb(221,237,234);
}
.highlight-blue_background {
	background: rgb(221,235,241);
}
.highlight-purple_background {
	background: rgb(234,228,242);
}
.highlight-pink_background {
	background: rgb(244,223,235);
}
.highlight-red_background {
	background: rgb(251,228,228);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(55, 53, 47, 0.6);
	fill: rgba(55, 53, 47, 0.6);
}
.block-color-brown {
	color: rgb(100,71,58);
	fill: rgb(100,71,58);
}
.block-color-orange {
	color: rgb(217,115,13);
	fill: rgb(217,115,13);
}
.block-color-yellow {
	color: rgb(223,171,1);
	fill: rgb(223,171,1);
}
.block-color-teal {
	color: rgb(15,123,108);
	fill: rgb(15,123,108);
}
.block-color-blue {
	color: rgb(11,110,153);
	fill: rgb(11,110,153);
}
.block-color-purple {
	color: rgb(105,64,165);
	fill: rgb(105,64,165);
}
.block-color-pink {
	color: rgb(173,26,114);
	fill: rgb(173,26,114);
}
.block-color-red {
	color: rgb(224,62,62);
	fill: rgb(224,62,62);
}
.block-color-gray_background {
	background: rgb(235,236,237);
}
.block-color-brown_background {
	background: rgb(233,229,227);
}
.block-color-orange_background {
	background: rgb(250,235,221);
}
.block-color-yellow_background {
	background: rgb(251,243,219);
}
.block-color-teal_background {
	background: rgb(221,237,234);
}
.block-color-blue_background {
	background: rgb(221,235,241);
}
.block-color-purple_background {
	background: rgb(234,228,242);
}
.block-color-pink_background {
	background: rgb(244,223,235);
}
.block-color-red_background {
	background: rgb(251,228,228);
}
.select-value-color-default { background-color: rgba(206,205,202,0.5); }
.select-value-color-gray { background-color: rgba(155,154,151, 0.4); }
.select-value-color-brown { background-color: rgba(140,46,0,0.2); }
.select-value-color-orange { background-color: rgba(245,93,0,0.2); }
.select-value-color-yellow { background-color: rgba(233,168,0,0.2); }
.select-value-color-green { background-color: rgba(0,135,107,0.2); }
.select-value-color-blue { background-color: rgba(0,120,223,0.2); }
.select-value-color-purple { background-color: rgba(103,36,222,0.2); }
.select-value-color-pink { background-color: rgba(221,0,129,0.2); }
.select-value-color-red { background-color: rgba(255,0,26,0.2); }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="8d2991fb-3bb7-4fd5-9e03-76c0f7693cab" class="page sans"><header><h1 class="page-title">Manual do Git</h1></header><div class="page-body"><h2 id="46b6ec37-ce26-448c-a022-62fdbcd9d88f" class="">00 - Configurações Iniciais</h2><pre id="4587e71a-ecc0-4162-a460-22635ba7aa42" class="code"><code>
sudo apt install git #instala o git no linux/debian e distros baseadas
git config --global user.name &quot;Seu Nome&quot; #Define identidade-Nome de usuário do GITHUB
git config --global user.email &quot;Seu Email&quot; #Define identidade - Email do GITHUB
#Isso marca o histórico com seu ID</code></pre><h2 id="d331fb24-69c3-4d40-9caf-fdbcdfa871e7" class="">02 - Ver todas as opções de configuração</h2><pre id="a362c0df-d284-4b9e-a6c9-e7321c85cf99" class="code"><code>man git #mostra o manual do git
git help #Mostra a pagina de ajuda do git 
git help comando #para acessar a ajuda de um comando em especifico
#Exemplo
git help clone #Abre o manual do comando especifico.</code></pre><h2 id="fd25f569-8f32-41ef-96de-2e1a8e3be470" class="">03 - Editor padrão</h2><p id="92c39275-7237-4031-b5e8-6435d90d98f2" class=""> </p><pre id="3cf8c74e-5370-464b-8203-eb5195bb9ead" class="code"><code>git config --global core.editor &quot;code -w&quot; #Substitui o editor padrão VIM pelo VSCODE</code></pre><h2 id="db2ea910-c24a-464f-9399-d18a5985bbd6" class="">04 - Ver quais configurações estão definidas</h2><pre id="3dd68e96-a716-4afe-9c29-08537ae84f87" class="code"><code>git config --list #mostra as configurações atuais</code></pre><h2 id="2f03b7fb-483a-4b5a-80e5-a9a465d833eb" class="">05 - Ativar color.ui </h2><p id="7311ca74-fb42-4e49-b66a-55efee3d6781" class="">Deixa o terminal mais amigável, marcando com cores, as ações tomadas</p><pre id="92469f05-acfc-4ee9-816e-e289ad603e4b" class="code"><code>git config --global color.ui true </code></pre><h2 id="51ce701a-fd18-4073-9ecf-338df01391ac" class="">06 - Para criar um repositório em um projeto.</h2><pre id="6ec8109e-72ba-45a7-a0f7-bba5530f894a" class="code"><code>#Na pasta do projeto
git init #Inicia um repositorio e cria uma pasta .git com as configuraçoes do projeto
ls -a #para ver se a pasta oculta foi criada</code></pre><p id="1bf81f96-52f8-4012-aff1-fc082952e35c" class=""><strong>ATENÇÃO</strong>
Todo o Histórico da versão e arquivos de configuração ficam dentro da pasta <strong>.git </strong>
Apagar a pasta <strong>.git</strong> vai ocasionar a perda de todo o histórico.</p><h2 id="fdf87acd-f7df-4f15-a71d-492de761cbc4" class="">07 - Fazer Commit</h2><pre id="d89e766a-7d8f-48fc-b8fe-ba75d49e8b24" class="code"><code>git add . #Prepara todos os arquivos da pasta para um ponto na História
git add nomeDoArquivo #Prepara um arquivo especifico para adicionar
git commit -m &quot;Commit Inicial&quot; #Cria o ponto na História
#o -m é para definir um comentario
</code></pre><h2 id="069184a8-0522-42de-b728-0de2a30b1192" class="">08 - Mostrar Histórico de mudanças</h2><pre id="a5e88e04-2a9a-4c00-bd80-3c526de79d32" class="code"><code>git log #Mostra um Historico dos pontos na História
git log --oneline #Histórico resumido
git log -n 5 #Traz os ultimos 5 commits
git log --grep=&quot;palavra chave&quot; #Busca por palavra chave</code></pre><h2 id="d96de53e-9fb6-470a-b6b0-a34b531feb1a" class="">09 - Os 3 estados </h2><pre id="3e0851b1-be6a-4d05-850f-5f69e9018072" class="code"><code>git init #Inicia um repositorio - Working Directory
git add . #Prepara todos os arquivos - Stage Area
git commit -m &quot;Commit Inicial&quot; #Cria o ponto na História Local Reposito/h2</code></pre><h2 id="06c51582-70db-4a26-9e60-65d2735dfe21" class="">10 - Ignorando arquivos e Diretórios</h2><pre id="8416ba33-effd-4a3e-9733-c2ec13ebe797" class="code"><code>touch .gitignore #Cria arquivo git ignore
nano .gitignore #Abre o arquivo para edição
#Para ignorar arquivos ou pastas basta adicionar seu nome no arquivo
git add .gitignore</code></pre><h2 id="0df418fa-b7a3-4da2-934f-8acc84fed356" class="">11 - Situação atual</h2><pre id="943a972e-a841-46f6-b483-b7b81e5eb352" class="code"><code>git status # Este comando mostra o estus atual </code></pre><h2 id="ecc8ec43-31ee-4c67-aaf5-00738fbc558a" class="">12 - Remover arquivos adicionados</h2><pre id="ad767b8e-33f7-4155-8935-9ebda2322fda" class="code"><code>git rm --cached nomeDoArquivo #Remove arquivos da Stage area</code></pre><h2 id="18e7d64c-426b-4a08-ba2d-d058792a5050" class="">13 - Adicionar por extensão</h2><pre id="bb5ef1d6-b796-4c0d-9491-009edfb638bc" class="code"><code>git add *.jsx # adicionar todos os arquivos com a extenção .js .php .html .ts etc..</code></pre><h2 id="7383f1c0-d73b-473b-ae56-34aed79cc9de" class="">14 - Ver as alterações dos nos arquivos</h2><pre id="ffdeda55-f651-4e4b-a580-6932ff9ef987" class="code"><code>git diff #mostra o que foi alterado</code></pre><h2 id="49dbb2e3-6263-4801-8616-4c9c49ffbd6a" class="">15 - Renomeando arquivo</h2><pre id="65c251c0-5b3a-4604-947c-29cbdbb0031b" class="code"><code>git mv nome.txt nomeNovo.txt #Renomear arquivo</code></pre><h2 id="073c3841-9d0e-4f7d-845d-afc6fb259995" class="">16 - Movendo arquivo</h2><pre id="3cf7476c-36ae-40fd-86a8-6612df446288" class="code"><code>git mv arquivo.txt pasta/arquivo.txt #Move arquivo</code></pre><h2 id="3ea1db85-33a6-460e-871f-a7de12ef799c" class="">17 - Restaurando um arquivo</h2><pre id="740bae89-9873-475c-8a73-f2cb73053eb6" class="code"><code>git restore arquivo.txt #restaura arquivo do Working Directory</code></pre><h2 id="ab293924-075b-4473-83f1-316994c9e545" class="">18 - Retirando arquivo do staged</h2><pre id="1462aa0b-b4b7-4151-ba38-7c02b79d8d61" class="code"><code>git restore --staged arquivo.txt #Remove arquivo do staged. 
git restore --staged . #Remove tudo do staged
#Bom pra quando é adicionado arquivos que não devem ser commitados </code></pre><h2 id="1fb14728-dbfc-40dc-8f3c-69a04300dff7" class="">19 - Corrigindo o Commit anterior</h2><pre id="a6db0f0e-f1de-4e25-a015-194d700cd588" class="code"><code>git commit --amend -m &quot;Mensagem&quot; #Corige o ultimo commit 
#OBS: Mais correto criar novo ponto na história
#então usar so quando adiciona um arquivo 
#Que não pode ficar na historia. 
#Como arquivo com dados sensiveis ou inuteis fora do escopo do projeto</code></pre><h2 id="e871d92e-efff-49fc-bd8d-eb3e623b4068" class="">20 - Restaurando arquivo</h2><pre id="27710a62-166b-49e9-a401-0182c2512f14" class="code"><code>git checkout hash -- nomeDoArquivo #O hash marca de qual commit vai restaurar o arquivo</code></pre><h2 id="b00ef9b5-4606-4919-94ac-85f106ceae23" class="">21 - Restaurando tudo</h2><pre id="4f40911b-1891-493c-859f-631aa368e1b0" class="code"><code>git revert HEAD~5 #O 5 são o numero de commits anteriores
#isso cria um nomo commit
git revert hash #mesmo resultado do anterior.</code></pre><p id="17dd16eb-2d73-4e43-a955-83066b5f09c4" class="">
</p></div></article></body></html>