# Tutorial de Criação de Temas para VScode
### Um tutorial conciso de tudo que você precisa saber como um iniciante feito eu, para montar seu próprio tema no VS Code 

#### Puxando Papo 🗨️

<div align="justify">
  
 Olá pessoa desenvolvedora, que assim como eu é apaixonada por pesonalização. Logo nós meus primeiros passos na programação, me esbarrei com o Vscode porém  não me senti atraido pela cara inicial que a interface me apresentou. Como é visivel  em meus projetos pessoais eu simplesmente adoro a combinação de verde com roxo e pessoalente, não achei nada que suprisse minha nessecidade de liberdade <s>e extravagancia</s>  .

#### Começando ▶️

Para estarmos na mesma página já deixo explicito que estaremos fazendo o uso pop_os! então, se algum comando for diferente na sua distribuição não se assuste, vou deixar um comentario ao lado do comando explicando o que precisa ser feito! ainda vamos chegar nisso, mas vale lembrar que nesse repositório também se encontra uma cola de tradução sobre o arquivo que vamos editar.
 
#### Instalação 🔧

Vamos começar com o mais obvil, precisamos do <strong> Vscode </strong>!  
  
  * entre em https://code.visualstudio.com/ e baixe a ferramenta para seu sistema operacional (.deb no nosso caso). <br>
  * Quando o download for concluido clique duas vezes no arquivo baixado e siga os passos para instala-lo em sua maquina (realmente não tem muito segredo).<br> <br>

  
Depois desse passo é hora de instalar o curl (Client Url) para instalar alguns arquivos com seu link de disponibilização <br>
 * no terminal para conferir se já o tem em seu computador use : <br>
   <code> curl --version </code>
  
 * caso não tenha, ainda no terminal:  <br> 
<code> sudo apt-get update</code> <br>
<code> sudo apt-get install curl </code> <br><br>
  
Tendo o Vscode e o Curl devidamente instalados, vamos precisar do <strong>Node.js</strong> (ambiente de Execução de javascript), vamos fazer seu download pelo nvm (Node Version Manager) Para escolher  versão do Node que usaremos.<br><br>
  * novamente no terminal use o seguinte comando curl para instalar o nvm: <br>
    <code>curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash</code><br>
  
  * agora selecione a verção que mais te agradar, eu recomendo a:<br>
    <code>sudo nvm 14</code> <br><br>
 
 Agora que os pilares da casa estão em ordem, vamos usar o gerenciador de pacotes javascript (npm) para instalar o gerador de extenções do Vscode (Yo Code), é importante que a partir de agora passemos a usar o terminal do vscode para estarmos na mesma página em questão de conceito. <br><br>
  
  * No terminal do  Vscode digite o seguinte comando: <br> 
  <code> sudo npm i -g yo generator-code</code> <br><br>
  * aguarde o gerador instalar e vamos dar inicio ao nosso projeto! <br>
  <code> sudo yo code </code><br><br>
  * use as setas direcionais para alterar as opções e enter para selecionar <strong>New Color Theme</strong> (Novo Tema de Cores)<br><br>
  * o gerador está te perguntando se você quer criar um tema novo ou importar um existente, no nosso caso, vamos criar um novo selecionando <strong>no, start fresh </strong> <br><br>
  * agora o gerador quer saber o nome do seu tema, seja bem craitivo!, tipo  MEU TEMA <br><br>
  * Escolha qual vai ser o indentificador da sua extensão, simplifique o nome do seu tema no caso do exemplo anterior seria meu-tema<br><br>
  * Adicione uma breve descrição do seu projeto <br><br>
  * a proxima pergunta é como o tema vai se apresentar ao usuario <br><br>
  * por fim, qual a base de cores você gostaria de usar? <br><br>
  * agora vamos usar o seguinte comando para ir para a pasta do nosso projeto<br><br>
  <code>sudo code ./meu-tema</code> no lugar de meu-tema, use o seu indentificador<br><br>
  
  #### Documentação 📄
  
  Moleza até agora certo? pronto pra por a mão na massa de verdade? deixa eu te apresentar a todos os arquivos que vamos trabalhar para quebrar esse gelo de estar em um ambiente que ainda não conhecemos bem. sem mais delongas vamos conhecer nossos arquivos <br><br>
  
  * <strong> gitignore </strong> blacklist do git<br><br>
  * <strong> CHANGELOG.md </strong> Registros de mudança do seu projeto<br><br>
  * <strong> README.md </strong> Arquivo de apresentação do seu projeto <br><br>
  * <strong> package.json </strong>  Arquivo onde vamos "Empacotar e etiquetar" o projeto <br><br>
  * Pasta <strong> .vscode</strong> Arquivos de configuração do Visual Studio Code <br><br>
  * Pasta <strong> themes </strong>, dentro do arquivo <strong> meu-tema.json </strong> é aqui que magia acontece! nossas cores estão aqui dentro esperando para ser alteradas<br><br>
  
  
  Existe varias coisas interessantes quando se trata de "coloração web" e eu gostaria de te contar duas delas, claro, seu uso fica totalmente ao seu criterio, mas com certeza só de saber esses conceitos, alguma diferença já vai fazer na hora da sua montagem. Primeiro vamos entender como interpretar uma cor em hexadecimal. Nossa escala numerica é de base decimal   ou seja, trabalhamos com 10 Algarismos, que vão de 0 a 9, na base hexadecimal Trabalhamos com 16 algarismos (0,1,2,3,4,5,6,7,8,9,a,b,c,d,e,f,) a marcação de um código de hexadecimal é representada por 3 duplas de 2 digitos <em>#XXYYZZ</em> onde # é a marcação de  hexadecimal XX são os digitos responsaveis pela  tonalidade vermelha , YY o verde E ZZ o azul , a intensidade dessas cores é definida em hexadecimal do 0(menos intenso) ao F(Mais intenso) Ou seja , #FF0000 é um vermelho muito forte, #FFFF00 (vermelho + verde) é amarelo #000000 é preto e assim por diante. Logicamente a maioria dos editores que vamos trabalhar interpretam esse código pra você, mas de qualquer forma é sempre bom você ter uma noção de qual cor se trata apenas de bater o olho (pode te poupar um tempo danado procurando aquele Hex especifico ). <br>
  
A por ultimo, uma forma simples de manter um bom jogo de cores na sua produção é apenas trabalhar com a regra 70/20/10. Com 5 matizes (pigmentos) distribuidos da seguinte forma:
3 cores que se comuniquem bem e 2 cores complementares entre si, dessas 3, uma vai ser usada em 70% da da produção , outra 20% e a ultima 10%. as outras duas complementares você usa pra textos e textos alternativos. Mas ai é com você, chega de papo e vamos por a mão na massa.
  
  #### Costomização 🎨
  
  Até que enfim o tópico que esperavamos, Aqui é onde vamos fazer testes e mais testes até chegar em um consenso. Por incrivel que pareça não temos muito o que falar da costumização em si 
 
  
  
  
  
  
  
  
  
  
  
  
  

  
  
  
</div>
