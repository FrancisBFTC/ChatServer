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

Nesta opção, na lista de usuários, cada usuário contém a opção de bloqueio através do símbolo **bloqueio vermelho**, que após clicado, o usuário pode se alto bloquear para aquele usuário em específico, não possibilitando o envio de emails, conversas em bate-papo e compartilhamento de arquivos, todas as opções são bloqueadas até que o usuário se alto-desbloqueie.

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

### <a name="block2"> 4.4 Bloqueio de todos os usuários </a>

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

O ChatServer conta com algumas dependências a nível de usuário e de desenvolvedor. Contém algumas operações essenciais para funcionamento do software, e são elas:

<a name="menu2"></a>
 ### Dependência do software
  * <a href="#kit"> Ambiente de execução Java(JRE) </a>
  * <a href="#imp"> Importação de bibliotecas </a>
  * <a href="#est"> Estrutura de pastas do software </a>
  
 ### Operações do software
  * <a href="#env"> Envio de dados para o servidor </a>
  * <a href="#aut"> Autenticação de dados criptografados </a>
  
  <a href="#menuprincipal">Voltar ao menu principal</a>
  
 ## 1. Dependência do software
  
 ### <a name="kit"> 1.1. Ambiente de execução Java(JRE) </a>
 
 O ChatServer é desenvolvido na linguagem de programação **Java**, por isso é necessário instalar a **JRE** (Java Runtime Environment) no computador. A JRE já contém as bibliotecas necessárias para a execução das funcionalidades do software. A JRE pode ser baixada no site da Oracle [clicando aqui](https://www.oracle.com/java/technologies/javase-jre8-downloads.html).

<a href="#menu2">Voltar ao menu</a>

 ### <a name="imp"> 1.2. Importação de bibliotecas </a>
 
 O software, a nível de desenvolvedor, utiliza a biblioteca **_apache-commons-net.jar_** onde contém classes responsáveis para envio de dados pelo _servidor FTP_. A classe principal utilizada pelo software é: **FTPClient** & **FTPClientConfig**. Estas classes contém métodos para upload e download de arquivos em servidores web. Um pacote no software é criado com vários métodos que executa operações de: Conexão com servidor web, Upload de arquivos, Download de arquivos, Pegar rede local, Pegar informações de arquivos, Pegar informações de mensagens, deletamento de arquivo, renomeamento de arquivo, desconexão do servidor web, entre outras funcionalidades.
  
  <a href="#menu2">Voltar ao menu</a>
  
  ### <a name="est"> 1.3. Estrutura de pastas do software </a>
 
  Uma estrutura de pastas são organizadas na instalação do software, são dentro destas pastas onde arquivos são baixados do servidor, arquivos que contém informações da conta na rede, informações de bloqueio/status, informações de mensagens internas e figurinhas emoticons. Para a parte de mensagens internas existem 2 pastas: **msgs** & **read**, onde em **msgs** são baixados arquivos com mensagens formatadas em HTML porém numa extensão diferente e **read** são todos os arquivos relacionado a mensagens que já foram lidas. Na pasta **log** são baixados informações de conta criptografados para o software ler e exibir. Em **imgs** contém todas as figurinhas do software. Na pasta organiza tem também o executável do ChatServer, um arquivo README com informações do desenvolvedor e um arquivo do microsoft word na extensão .docx com instruções de utilização do software.
  
  <a href="#menu2">Voltar ao menu</a>
  
  ## 2. Operações do software
  
  ### <a name="env"> 2.1. Envio de dados para o servidor </a>
  
  O ChatServer utiliza um servidor web hospedado para fazer comunicação de dados. Os dados de conta e emails eletrônicos internos são armazenados neste servidor. No servidor web também contém uma estrutura de pastas organizadas que armazenam arquivos, tais arquivos são baixados pelo software ao decorrer das operações efetuadas pelo usuário e são enviados novamente para o servidor.
  
  <a href="#menu2">Voltar ao menu</a>
  
  ### <a name="aut"> 2.2. Autenticação de dados criptografados </a>
  
  Alguns dos arquivos baixados, enviados e atualizados no servidor são os **arquivos de conta**, são esses arquivos que possibilitam fazer a **autenticação de login**, pois contém dados criptografados em AES-256 bits utilizando 2 chaves privadas. O software se encarrega se executar a descriptografia dos dados utilizando o mesmo método que criptografou, assim ele verifica se os dados inseridos no campo de login são os mesmos que os dados armazenados no arquivo, caso sim, o usuário é logado na sua conta do ChatServer, caso não, o software exibe uma mensagem de erro.
  
  <a href="#menu2">Voltar ao menu</a>
 
 <a href="#menuprincipal">Voltar ao menu principal</a>
 
 ### Agradecimentos
 
 Se chegou até aqui, muito obrigado por ler esta documentação! É uma honra poder desenvolver softwares open-sources e comerciais para todos os usuários e programadores. Agradecimentos BFTC!
 
 Ass.: Wender Francis da BFTCorporations.
 
 Site Oficial : [bftcorporations.mywebcommunity.org](http://bftcorporations.mywebcommunity.org/Courses)
 
 [Voltar ao repositório](https://github.com/FrancisBFTC/ChatServer/)
