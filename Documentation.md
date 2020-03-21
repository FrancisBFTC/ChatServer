**********************************************************************************
<h1 align="center"><a name="top">Documentação do ChatServer</a></h1>

Bem vindo a documentação do ChatServer! aqui é demonstrado todas as funcionalidades atuais do software, descrições gerais e técnicas. Se optar por ler um assunto em específico abaixo contém um menu de atalho, se não, continue rolando para ler toda a documentação:
  
  <a name="menuprincipal"></a>
  * <a href="#desc1"> Descrições Gerais </a>
  * <a href="#desc2"> Descrições Técnicas </a>
  * <a href="#util"> Utilização do software </a>
 
<a name="desc1"><h1 align="center"> ---------- Descrições Gerais ---------- </h1></a>

O ChatServer é um software de compartilhamentos de arquivos e bate-papo em rede interna local. Com o software poderá se cadastrar para criar o usuário, enviar arquivos de um computador para outro mediante a autorização do usuário, enviar mensagens temporárias (bate-papo) e mensagens permanentes (Email interno). Logo abaixo contém o menu de navegação demonstrando as funcionalidades do ChatServer:

<a name="menu1"></a>
### Cadastro no ChatServer:
  * <a href="#cad"> Cadastrando a conta </a> 
  * <a href="#log"> Logando na conta</a> 
  
### Métodos de mensagens:
  * <a href="#mens1"> Mensagens Temporárias (bate-papo) </a>
  * <a href="#mens2"> Mensagens permanentes (Email interno) </a>
  
### Menu individual do software:
  * <a href="#chat"> Chat privado </a>
  * <a href="#email"> Email interno individual </a>
  * <a href="#block1"> Bloqueio de usuário espefícico </a>
  * <a href="#comp"> Compartilhamento de arquivos </a>
  
### Menu geral do software:
 * <a href="#email2"> Email interno geral </a>
 * <a href="#conf"> Configurações da conta </a>
 * <a href="#infs"> Informações da conta </a>
 * <a href="#block2"> Bloqueio de todos os usuários </a>
 * <a href="#status"> Ativação/Desativação de Status </a>
 * <a href="#desl"> Deslogamento da conta </a>

<a name="util"><h1 align="center"> ---------- Utilização do Software ---------- </h1></a>

## 1. Cadastro no ChatServer

### <a name="cad"> 1.1 Cadastrando a conta </a>

  Esta é a tela de cadastro, onde os usuários de cada computador da rede irá inserir seu nome, usuário, senha e confirmação de senha. O usuário vai acessar sua conta através do usuário inserido e sua senha, porém o que vai aparecer para outros usuários é o seu **nome**. Os dados de cada conta que é cadastrada é enviada por meio de um servidor FTP para um servidor web, armazenando arquivos com o número de IP e com dados encriptados em criptografia AES-256 bits.
  
  ![](/Imagens/ChatServer1.png)
  
  <a href="#menu1"> Voltar ao menu </a>
  
### <a name="log"> 1.2 Logando na conta </a>

   Após cadastrado, o usuário poderá inserir seus dados nos campos e logar na conta. Esta é a primeira tela que aparece no sistema e quando o usuário loga na sua conta, durante o processo, os dados gravados no servidor web são requisitados e descriptografados utilizando o mesmo método de criptografia com 2 chaves privadas, se os dados decriptados forem corretos, o usuário é redirecionado para a 2ª tela que contém todas as opções de manuseio do software.
  
  ![](/Imagens/ChatServer2.png)
  
  <a href="#menu1">Voltar ao menu</a>
  
## 2. Métodos de mensagens

   ### <a name="mens1"> 2.1 Mensagens Temporárias (bate-papo) </a>
   
   Neste método o usuário escolhe um usuário para conversar. Ele clica no usuário específico e envia mensagens através de um campo onde ele pode inserir emoticons, as mensagens são enviadas em rede local por meio de Sockets, isso significa que se o respectivo usuário que ele estiver conversando esta offline, não será possível enviar uma mensagem.
   
   ![](/Imagens/ChatServer3.png)
   
   <a href="#menu1">Voltar ao menu</a>
   
   ### <a name="mens2"> 2.2 Mensagens permanentes (Email interno) </a>
   
   No ChatServer também contém a opção de "cartinha" para enviar uma mensagem permanente ao usuário, mesmo se ele estiver offline, ele receberá a mensagem mais tarde. O que também é chamado no programa de "Email eletrônico interno" pois funciona tal como um, onde os usuários poderão ver mensagens com assuntos a qualquer hora.
   
   ![](/Imagens/ChatServer4.png)
   
   <a href="#menu1">Voltar ao menu</a>
  
## 3. Menu individual do software

### <a name="chat"> 3.1 Chat privado </a>

No chat privado os usuários poderão conversar apenas entre eles, ou seja, aqueles que estiverem online poderão conversar de forma privada. No chat é possível enviar palavras formatadas, como: negrito, itálico e sublinhado. Também é possível enviar figurinhas de emotions. Os usuários recebem as mensagens instântaneamente por rede local, isto enquanto o software está aberto. O usuário poderá fechar a janela de chat e abrir quando quiser que as mensagens ainda estarão lá, porém a partir do momento que ele fecha o software, o painel de mensagens é zerada dando início a novos textos - isso significa que são **_mensagens temporárias_**.

 ![](/Imagens/Demo12.png)
 
 <a href="#menu1">Voltar ao menu</a>
 
### <a name="email"> 3.2 Email interno individual </a>

No caso do Email interno individual, cada usuário poderá enviar uma mensagem para um usuário específico, ou seja, clicando na opção de "cartinha" no menu do usuário, apenas aquele usuário verá as mensagens que são enviadas. O usuário tanto que pode escrever uma mensagem definindo um assunto quanto que pode verificar as mensagens recebidas em ordens de um usuário específico, as mensagens mais recentes são organizadas no topo, dando a possibilidade de excluí-las a hora que quiser - isso significa que são **_mensagens permanentes_**.

![](/Imagens/Demo27.png)

<a href="#menu1">Voltar ao menu</a>

### <a name="block1"> 3.3 Bloqueio de usuário específico </a>

--texto--

![](/Imagens/Demo47.png)
![](/Imagens/Demo48.png)

<a href="#menu1">Voltar ao menu</a>

### <a name="comp"> 3.4 Compartilhamento de arquivos </a>

Na lista de usuários, cada usuário contém opções que poderão ser feitas apenas para ele em específico, uma delas é a opção com o símbolo de "arquivo" - esta opção é responsável por possibilitar uma escolha de um arquivo do computador e enviar para o usuário em questão, porém o usuário que receberá o arquivo também vai receber uma notificação perguntando se ele quer receber o arquivo, caso ele aceitar, o arquivo é recebido e a mensagem de confirmação é enviada para o usuário de origem. Não é possível enviar vários arquivos ao mesmo tempo.

![](/Imagens/Demo35.png)
![](/Imagens/Demo36.png)
![](/Imagens/Demo37.png)

<a href="#menu1">Voltar ao menu</a>

## 4. Menu geral do software
  
  ### <a name="email2"> 4.1 Email interno geral </a>
   
   Seguindo as opções do **Menu geral do software**, o símbolo de **carta** possibilita que os usuários possam enviar mensagens para todos os usuários ao mesmo tempo, ou visualizar mensagens de todos os usuários em um único painel, diferentemente do **Email interno individual** que as mensagens são de um usuário em específico.
   
![](/Imagens/ChatServer5.png)

<a href="#menu1">Voltar ao menu</a>

### <a name="conf"> 4.2 Configurações da conta </a>

Nesta tela, aberta com a opção do símbolo de **engrenagem**, poderá alterar o usuário e a senha, exceto o **_nome_** que uma vez criado não pode ser alterado. No exemplo da imagem a senha era **user123** e está sendo alterado para **user001**, logo após uma mensagem de confirmação é exibida.

![](/Imagens/ChatServer6.png)
![](/Imagens/ChatServer7.png)

<a href="#menu1">Voltar ao menu</a>

### <a name="infs"> 4.3 Informações da conta </a>

Na tela de informações, clicada na opção com o símbolo de **i**, o usuário poderá ver todas as informações da sua conta: O ip do computador que possibilita a comunicação em rede, o nome da conta, o usuário da conta, a senha da conta e o status de online/offline.

![](/Imagens/ChatServer8.png)

<a href="#menu1">Voltar ao menu</a>

### <a name="block"> 4.4 Bloqueio de todos os usuários </a>

Quando é clicado no símbolo de **bloqueio vermelho**, uma mensagem de confirmação é exibida perguntando se o usuário realmente deseja ficar bloqueado para todos na rede, caso sim, nenhum usuário conseguirá executar nenhuma operação para ele, pois todas as opções do software são bloqueadas para aquele usuário.

![](/Imagens/ChatServer9.png)

<a href="#menu1">Voltar ao menu</a>

### <a name="status"> 4.5 Ativação/Desativação do status </a>

No menu geral, também existe a opção de **bolinha verde** que indica que o usuário está online na rede, neste momento todos os usuários verão que este usuário está online, porém caso o usuário decida clicar nesta bolinha, a cor é mudado pra vermelho e todos os usuários verão que ele está **offline**, ou seja, uma forma de disfarçar quando se deseja que nenhum usuário o incomode.

![](/Imagens/ChatServer10.png)
![](/Imagens/ChatServer11.png)

<a href="#menu1">Voltar ao menu</a>

### <a name="desl"> 4.6 Deslogamento da conta </a>

Para deslogar na conta basta clicar na última opção e é sempre indicado que desloque clicando nesta opção, assim o sistema sempre encarregará de fazer as configurações necessárias para mostrar a todos os usuários que ele está offline.

![](/Imagens/ChatServer12.png)

<a href="#menu1">Voltar ao menu</a>

## <a name="lim"> 5. Limitações do software </a>

Quanto a limitações, o software tem algumas restrições e são elas:

* O usuário não pode modificar o **nome** da conta.
* Cada computador na rede deve ter apenas **1 conta**.
* O software não é capaz de enviar vários arquivos ao mesmo tempo.
* É obrigatoriamente recomendado que cada computador na rede local tenha o **ip estático**.
* A opção de **Alerta sonoro** ainda não foi desenvolvida, poderá ser implementada nas próximas versões.
* É recomendado que o software seja instalado numa pasta com permissão de acesso a arquivos, fora isso o software não é capaz de executar suas operações.
  
  <a href="#menu1">Voltar ao menu</a>
  
<a name="desc2"><h1 align="center"> ---------- Descrições Técnicas ---------- </h1></a>

O GhostScan utiliza determinados procedimentos para realizar suas principais tarefas, contando com - dependências de bibliotecas, estrutura de pastas, kit de desenvolvimento java, configurações no sistema operacional e arquivos em lotes do windows, as principais tarefas selecionadas com níveis prioritários são:

<a name="menu2"></a>
 ### Dependência do software
  * <a href="#kit"> Kit de desenvolvimento Java(JDK) </a>
  * <a href="#conf"> Configurações do sistema operacional </a>
  * <a href="#imp"> Importação de bibliotecas </a>
  
 ### Algoritmos & Organização
  * <a href="#env"> Envios de email & scanners nativos </a>
  * <a href="#est"> Estrutura de pastas organizadas </a>
  * <a href="#arq"> Arquivos em lote do Windows (Batch File) </a>
  * <a href="#out"> Outros algoritmos </a>
  * <a href="#info"> Informação de versões & atualização </a>
  
  <a href="#menuprincipal">Voltar ao menu principal</a>
  
 ## 1. Dependência do software
  
 ### <a name="kit"> 1.1. Kit de desenvolvimento Java(JDK) </a>
 
 Após lermos as <a href="#desc1">Descrições Gerais</a> sabemos que o GhostScan funciona como um **programador** criando programas.
 Isto significa que ele precisa criar arquivos fontes que contém classes do Java, compilar esses arquivos e depois gerar o
 executável. Para todos esses procedimentos é preciso ter a JDK instalada na máquina, pois é ela que possibilita as ferramentas
 e classes necessárias para desenvolver em linguagem java e gerar o keylogger, as principais ferramentas utilizadas são: jar.exe e javac.exe. Isto inclui arquivos JARs responsáveis por guardar classes e métodos para a programação em Java. Caso o usuário não tenha a JDK em sua máquina, deveria fazer o [Download da JDK](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) do site oficial da oracle. A ferramenta deve ser instalada no diretório **C:\\Program Files\\Java\\**(Por padrão o JDK já instala automaticamente a JRE que também é necessária para execução de aplicações em Java).

<a href="#menu2">Voltar ao menu</a>

 ### <a name="conf"> 1.2. Configurações do sistema operacional </a>
 
 Na instalação do software GhostScan, o instalador já executa um arquivo executável extra para as configurações do sistema
 operacional. Este arquivo contém todos os comandos cmd necessários para definir variáveis de ambiente, criando as variáveis
 **JAVA_HOME**, **CLASSPATH** e **PATH** para setar os conteúdos delas com diretórios do JDK e JRE. Isto é necessário pois pra
 compilar as classes do keylogger para .class e criar o executáveis JARs, o sistema utiliza as ferramentas jar e javac o que
 exigem obrigatoriamente as definições das variáveis de ambiente. As variáveis são setadas com os seguintes valores:
 
  * JAVA_HOME = "C:\Program Files\Java\jdkxxxx\"
  * CLASSPATH = ";%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar;%JAVA_HOME%\lib\dt.jar;"
  * PATH = "%PATH%;%JAVA_HOME%\bin;"
  
  **Observações:** _O **xxxx** em **JAVA_HOME** seria a versão do JDK, consulte o nome da pasta dentro do diretório **Java**_
  
  <a href="#menu2">Voltar ao menu</a>
  
  ### <a name="imp"> 1.3. Importação de bibliotecas </a>
 
  Após todas as configurações serem feitas, algumas bibliotecas são importadas no projeto antes mesmo do desenvolvimento, e são elas: **JNativeHook**, **Commons-email** & **javamail**. O **JNativeHook** é o responsável por disponibilizar métodos para leitura de mouse e teclado de forma nativa. Diferentemente dos **_KeyEvents_** que são padrões do JDK que ler o teclado apenas
na Interface do software, os **_NativeKeyEvents_** ler o teclado fora da interface, ou seja, em qualquer lugar do computador.
Isto é o que permite o Keylogger escanear informações de teclas. O **Commons-email** e **javamail** contém classes que possibilitam o envio de **emails**. Estas classes contém métodos para autenticação de login, definição de mensagens, envio de mensagens,etc... A biblioteca também contém a classe para envio de emails formatados em Html, como o: **HtmlMail** e a classe 
para envio de mensagens sem nenhuma formatação, como o: **SimpleMail**. Atualmente estas bibliotecas sofreram algumas atualizações com novas versões, o que explicam os possíveis bugs que poderiam gerar no software caso o computador do usuário esteja programado para atualizar o java automaticamente, porém na versão 2.0 do GhostScan a atualização automática também será disponível, o que eliminará as possíveis falhas por conta das atualizações do Java.
  
  <a href="#menu2">Voltar ao menu</a>
  
  ## 2. Algoritmos & Organização
  
  ### <a name="env"> 2.1. Envios de emails & scanners nativos </a>
  
  Como descrito em **Importação de bibliotecas**, o software trabalha com classes e métodos responsáveis por enviar emails e 
  escanear mouse/teclado de forma nativa. A classe de cada Keylogger implementa as interfaces **NativeMouseInputListener** e **NativeKeyListener** na qual cada interface contém métodos que são gerados para detectar movimento do mouse, cliques do mouse, pressionamento de teclas,etc... As posições do mouse são capturadas e são guardados textos em variáveis que são resultados de valores intermediários das regiões da tela. Já as teclas são concatenadas em variáveis a cada pressionamento, comparações são feitas para detectar cada tecla escaneada armazenando o resultado em variável global. Após todas as informações serem armazenadas, a cada intervalo de tempo (ou se cliques for detectados), As classes de email realizam autenticação dos dados de email inseridos no keylogger, a porta e o servidor do Gmail são setados e a classe envia um texto para o email, formatado em Html concatenado com as variáveis que guardam informações escaneadas.
  
  **Observaçoes:** _Neste caso, o GhostScan só criam keyloggers que utilizam o servidor do **Gmail**. Na versão 2.0 será acrescentado opções para escolher outros servidores, por exemplo: Hotmail, Outlook,etc..._
  
  <a href="#menu2">Voltar ao menu</a>
  
  ### <a name="est"> 2.2. Estrutura de pastas organizadas </a>
  
  O keylogger para ser gerado precisa de uma **Estrutura de pastas** pré-criadas. Estas pastas são instaladas no ato da Instalação do software e o diretório origem do GhostScan fica exatamente junto com estas pastas. Neste diretório estruturado contém pastas de bibliotecas como o JNativeHook e o Commons-email, pastas que contém bibliotecas do Java, Pasta de imagens do GhostScan, arquivos de manifestos, arquivos em lotes do windows para compilação e a pasta que é gerada os arquivos compilados do keylogger. Esta estrutura de pastas são nada mais nada menos os que ficam compactados com o JAR do arquivo keylogger, portanto esta estrutura é necessária para a geração do arquivo executável.
  
  <a href="#menu2">Voltar ao menu</a>
  
  ### <a name="arq"> 2.3. Arquivos em lotes do Windows (Batch Files) </a>
  
**_Batch Files_** ou **_Arquivos .bat_** são arquivos em lotes do Windows para armazenar e executar comandos do CMD, conhecido como **Prompt de comando**. Alguns softwares necessitam de operações utilizando estes comandos, como é o caso do GhostScan. Um exemplo é quando o software executa outro software que precisa de parâmetros e argumentos.. o GhostScan executa as ferramentas JAR e JAVAC para compilação do código do Keylogger.. como também executa as mesmas ferramentas para compilação e geração do executável do vírus **Ghost**. Estas ferramentas utilizam parâmetros via linha de comando utilizando CMD, o que o GhostScan faz é usar as mesmas linhas de comando alterando e armazenando variáveis em arquivos BAT, pois para cada arquivo gerado há um nome diferente, esses nomes são passados em variáveis BAT. Outra questão é a inicialização automática, onde o keylogger se auto-copia para um certo diretório do computador, Esta cópia é possibilitada através de um comando CMD, porém não utiliza os arquivos BATs desta vez, isto é feito no próprio código. Para setar as variáveis de ambiente no ato da instalação é a mesma coisa - um arquivo BAT é gerado e executado. O que será alterado na versão 2.0 será isto, o software não mais utilizará os Batch Files mas sim: utilizará os comandos no próprio código do keylogger.

<a href="#menu2">Voltar ao menu</a>

 ### <a name="out"> 2.4. Outros algoritmos </a>

Além de algoritmos de Scanners e emails, o GhostScan trabalha com algoritmos de detectar informações de rede, IP e ScreenShot da tela. Porém é importante ressaltar que não é o GhostScan que utiliza esses algoritmos - É o keylogger que foi gerado pelo GhostScan. Então como prioridade o que software faz: Ele verifica as opções selecionadas e inseridas do usuário, guarda em variáveis e faz comparações, dependendo do resultado da comparação o software armazena inúmeros algoritmos em formato de texto (String) em variáveis, após isso, estas variáveis são concatenadas com outras que seriam padrões para todos os keyloggers, o que nos dar **23 possibilidades** de algoritmos diferentes (Claro que em outras versões do GhostScan as possibilidades irão muito além disso), então é escrito um arquivo com o conteúdo das possíveis variáveis concatenadas, este arquivo é compilado e gerado o JAR que se transforma no keylogger.

Agora falando dos algoritmos específicos para outras operações: O ScreenShot da tela utiliza classes que verifica o tamanho da tela com a classe **Dimension**, tira o screenshot através da classe **Robot**, armazena o Screenshot em um buffer de imagem pela classe **BufferedImage** e escreve a imagem no sistema através da classe **ImageIO** com o tipo JPEG e um nome pré-definido. Este nome da imagem é usado para enviar como anexo para o email. Já nas informações de rede, o algoritmo utiliza a classe **InetAddress** para detectar informações de IPs internos, nome do computador e servidores locais, utiliza também a classe **Inet4Address** para pegar o nome do servidor local. No caso das placas e interfaces de redes instaladas, as informações são obtidas da classe **NetworkInterface** e percorre informações completas através de _Enumerações_ também utilizando a classe **InterfaceAddress**. Para cada classe desta existem métodos responsáveis por tais operações. O IP público é obtido fazendo uma requisição via URL do site [checkip amazonaws](http://checkip.amazonaws.com), a informação é capturada por um _leitor bufferizado_ com _Streams de Entrada_. Cada algoritmo desse armazena informações em variáveis, onde tais variáveis são concatenadas e enviadas para o email.

<a href="#menu2">Voltar ao menu</a>

  ### <a name="info"> 2.5. Informações de versões & Atualização </a>
  
  Após ler toda a documentação do GhostScan, aqui são destacadas todas as funcionalidades acrescentadas e correções futuras do GhostScan 2.0:

**Correções na versão 2.0 --->**

 * O sistema da versão 1.0 foi feito para ambientes Windows, mesmo que "algumas" funcionalidades executam no linux. No GhostScan 2.0 o software vai identificar o sistema operacional e terá algumas operações diferentes em cada plataforma, o que possibilitará executar todas as funcionalidades em qualquer plataforma: Windows, Mac & Linux.
 
 * O GhostScan para gerar o keylogger precisa da JDK instalada. Na versão 2.0, o software irá identificar se existe uma JDK instalada e se as variáveis de ambiente estão setadas, caso não estiver ele executa o JDK da própria pasta raiz do software, sem mesmo ter que precisar configurar variáveis de ambiente. Porém se existir a JDK mas as variáveis de ambiente não estão setadas, o software vai apenas setar as variáveis.
 
 * Como descrito na documentação, o software executa os arquivos .bat pré-gerados para efetuar alguma operação. Na outra versão isso não será necessário, pois esta parte será corrigida. Os comandos serão efetuados pelo próprio algoritmo do software, o que diminui a quantidade de arquivos da pasta raiz.

**Novas funcionalidades na versão 2.0 --->**

 * No sistema poderá ser selecionado a opção para enviar **Geo-localização aproximada** para o email baseado no IP público. Isto significa que: se o alvo tem um pendrive configurado para auto-execução e contém o keylogger lá dentro, o monitorador poderá saber a região que o alvo está se ele estiver utilizando um computador em outro local (com o respectivo pendrive), por exemplo: Numa lan house. O sistema enviará informações completas de latitude e longitude, região, cidade,etc...
 
 * Tornar pendrives auto-executáveis: O GhostScan poderá também além de gerar um keylogger, tornar um pendrive auto-executável e copiar o keylogger para ele, isto significa que na inserção do pendrive em qualquer computador, o keylogger será copiado para o computador e executado automaticamente.
 
 * Outro sistema de camuflagem implementado no GhostScan é o de **Conversão de tipos**. Após o keylogger ser gerado no formato **.jar**(Arquivo executável java), o usuário poderá escolher o conversor de tipos para converter do formato .jar para .exe (Arquivo executável do windows), dando uma maior camuflagem e possibilitando também a próxima funcionalidade.
 
 * Com um executável do tipo **.exe** o usuário poderá escolher no sistema de camuflagem um **ícone** para o keylogger, o GhostScan por padrão terá no seu sistema vários ícones prontos de outros softwares para ser escolhido, porém o usuário também poderá escolher seu próprio ícone em diretórios do seu computador.
 
 * Além do GhostScan ter opções de escanear teclado, mouse, ip, rede & screenshot, o software terá mais uma opção: Escanear históricos de navegadores. Todos os sites que o alvo pesquisar, o keylogger capturará todo o histórico dos browsers e enviará para o email do monitorador.
 
 * Na versão 1.0 o usuário só consegue gerar o keylogger na pasta raiz do programa, o que significa que dependendo da pasta, o usuário precisa ter permissão de escrita naquele diretório e sabemos que nem todos os diretórios tem esta permissão, Exemplo: Arquivos de programas. O sistema operacional automaticamente bloqueia a opção de escrita, a não ser que o usuário faça manualmente configurações de liberar permissão de administrador, porém na versão 2.0 não será necessário - Existirá um novo campo para o usuário escolher onde gostaria de criar o seu keylogger, ele poderá criar até na área de trabalho se quiser, o que elimina o fato de possíveis conflitos de permissão.
 
 * Atualmente o GhostScan trabalha com o servidor [smtp.gmail.com](https://gmail.com) na porta 447, o que significa que o keylogger só envia informações para contas de **Gmail**. Na versão 2.0, em vez do usuário ter que precisar criar uma nova conta do gmail apenas para monitoramento, ele pode criar contas em qualquer servidor, pois o GhostScan 2.0 terá a opção de escolher em qualquer servidor desejaria que o keylogger estivesse configurado, se seria o servidor do **hotmail** ou do **outlook** ou outros... Então isto vai depender da conta que o usuário inserir nas configurações do keylogger.
 
 * Por último mas não menos importante: O sistema de atualização automática estará disponível na versão 2.0. O software terá um executável de atualização junto na pasta de instalação que irá identificar se há uma nova versão do GhostScan no site da BFTC, se houver, o sistema alertará o usuário pedindo a confirmação para fazer a atualização do sistema. O software irá fazer download do site oficial, excluir os diretórios antigos e reinstalar a outra versão do GhostScan. Então o sistema de atualização sempre executará quando o computador do usuário ligar.
 
 **Detalhes importantes:** O Software GhostScan tem a versão **free Trial** neste mesmo repositório e a versão **comercial**. A versão Free Trial funciona apenas em 3 dias e bloqueia alguns recursos, sendo utilizado apenas para teste do programa. A versão comercial funciona por tempo ilimitado e contém todos os recursos descritos até aqui. A versão Free Trial também está disponível no site da [BFTCorporations](http://bftcorporations.mywebcommunity.com/Courses/) para [Download](http://bftcorporations.mywebcommunity.org/Downloads/GhostScan1.0/), já para ter acesso a versão paga o usuário precisaria ter um ID e senha criado pelo administrador após a compra do software. Após a compra, o usuário poderia acessar este mesmo ID para baixar a versão 2.0 do software, porém nesta próxima versão não será necessário efetuar esta mesma operação já que o software terá o sistema de **Atualização automática**, sendo assim, o usuário terá direito a todas as atualizações após a compra, incluindo as versões **Mobile App** do GhostScan.
 
 **Observações:** _Estes códigos, documentação e software estão protegidos por direitos autorais. Portanto é proibido a cópia/plágio, a distribuição ou venda do software/código descrito pelo Art. 184 do Código Penal - Decreto Lei 2848/40._
 
 <a href="#menuprincipal">Voltar ao menu principal</a>
 
 ### Agradecimentos
 
 Se chegou até aqui, muito obrigado por ler esta documentação que levou 2 dias para ser concluída! É uma honra poder desenvolver softwares open-sources e comerciais para todos os usuários e programadores. Agradecimentos BFTC!
 
 Ass.: Wender Francis da BFTCorporations.
 
 Site Oficial : [bftcorporations.mywebcommunity.org](http://bftcorporations.mywebcommunity.org/Courses)
 
 [Voltar ao repositório](https://github.com/FrancisBFTC/GhostScan-JAVA/)
