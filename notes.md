#28/01/2026

Faça esse curso de IA para Dados e:
Descubra como a automação pode revolucionar a sua rotina de trabalho.
Domine ferramentas e técnicas para construir fluxos de trabalho inteligentes.
Economize tempo e reduza erros ao eliminar tarefas repetitivas.
Desenvolva a capacidade de identificar e automatizar processos ineficientes.
Aprenda a aplicar a automação em diferentes cenários, do pessoal ao corporativo.
Aulas
Construindo uma automação no Make  Ver primeiro vídeo
0 / 12
52min
Praticando automações no Make
1 / 2
0min


@01-Construindo uma automação no Make 

@@01
Apresentação

Você, como gestor ou gestora, ou mesmo colaborador em uma organização, já considerou automatizar tarefas repetitivas relacionadas a aplicativos digitais no seu trabalho para acelerar processos? O Make é uma ferramenta projetada para executar exatamente isso: automatizar tarefas repetitivas por meio de aplicativos digitais, operando de forma autônoma, com a possibilidade de especificar a duração e a quantidade de repetições desejadas. Interessado em entender mais sobre isso? Vamos aprender juntos.

Apresentando a instrutora
Antes de começarmos, permita-me apresentar. Meu nome é Mirla, sou instrutora na Alura.

Audiodescrição: Mirla é uma mulher de pele clara, com cabelos pretos, cacheados e de tamanho médio. Ela está usando uma blusa preta e óculos de grau com armação redonda. Mirla será a instrutora que acompanhará durante todo este curso.
Explorando o caso de uso no Bytebank
Na situação apresentada, trabalharemos em um banco, o Bytebank, onde recebemos diversos e-mails com diferentes conteúdos. Um desses conteúdos consiste em várias perguntas dos clientes, que poderiam ser respondidas a partir do FAQ, a cartilha de Perguntas e Respostas dos Clientes. Para facilitar a velocidade com que esses e-mails são respondidos, podemos criar um fluxo no Make. Esse fluxo, que está na tela, permite receber um e-mail, processá-lo, verificar se pode ser respondido pelo FAQ e, caso positivo, gerar e enviar a resposta automaticamente. Caso contrário, o fluxo ajuda a organizar as pastas dos e-mails para identificar a categoria do e-mail.

Iniciando o aprendizado sem pré-requisitos
Gostaria de saber como podemos implementar isso? Este curso não possui pré-requisitos. Não será necessário estruturar nenhum código, pois o Make é muito simples de utilizar. Vamos estudar juntos?

@@02
Preparando o ambiente

Para nosso projeto iremos utilizar o Make, Microsoft e Groq. Usaremos o Make para construir uma automação e construímos um fluxo, a conta do Microsoft para acessar seus serviços de e-mail e planilhas (excel) e o Groq para acessar os modelos de inteligencia artifical. Para cada uma das ferramentas, conseguimos executar nosso projeto de forma gratuita.
1. Make
O Make é uma plataforma de automação sem código que permite conectar aplicativos e criar fluxos de trabalho automatizados de forma visual e intuitiva. Com mais de 2.000 aplicativos pré-construídos, ele capacita usuários a integrar ferramentas e automatizar processos sem necessidade de programação. Para desenvolver o projeto deste curso, você precisará de uma conta no Make

Para fazer uma conta no Make acesse o link https://www.make.com/en/register e siga os passos para a criação da conta.

Para o projeto desse curso a conta gratuita funciona bem, mas atente-se, a conta gratuíta tem algumas limitações de uso contínuo. Saiba mais sobre os limites da conta gratuita e outros planos nesse link.

2. Groq
O Groq disponibiliza chaves gratuitas, nos permite aplicar modelos inteligentes e personalizadas com base na necessidade do projeto. Para desenvolver o projeto deste curso, você precisará de uma chave de API, que vamos aprender, a seguir, como obtê-la!

O primeiro passo é acessar a página do Groq nesse link que permite a solicitação de uma chave. Para concluir esse passo, é fundamental que você crie uma conta na plataforma, pois a chave de API é gerada exclusivamente para pessoas cadastradas.

Com a conta cadastrada, siga os passos abaixo para coletar a chave API:

1 - Na página de API Keys, clique no botão Create API Key.

Imagem do botão Create API Key destacado

2 - Na janela que será aberta, insira um nome para a chave. Escolha um nome que facilite a identificação do projeto relacionado e clique em Submit.

3 - Após criar a chave, uma nova janela será exibida. Copie a API Key gerada e armazene-a em um local seguro. A chave não será exibida novamente. Depois, clique em Done.

Imagem da janela com a API Key gerada e o botão Done destacado

4 - Retornando à página de API Keys, você verá uma lista com as chaves criadas, incluindo opções para editar o nome, excluir uma chave ou criar uma nova para outros projetos.

3. Microsoft
A Microsoft oferece soluções como o Outlook para e-mails e o Excel para planilhas e análises de dados.

Para acessar os serviços da Microsoft é necessário ter uma conta cadastrada. Você pode criar uma conta na Microsoft acessando [o site oficial]https://signup.live.com/signup) e seguir os passos para criar a conta.

O ideal é que você utilize os serviços Microsoft nesse curso. Caso isso não seja possível, recomendamos utilizar os serviços do Google. Mais adiante nas atividades temos uma explicação de como usá-los.
3.1 Outlook
Usaremos o Outlook como ferramenta para receber e-mails do projeto. Nele, teremos uam etapa que foca em organizar os e-mails recebido dentro da conta por categoria definidas em pastas. Para isso, é necessário já terem sido criadas as pastas. Vamos entender como criá-las e quais categorias utilizar.

1 - Na aba da sua conta, localize a aba de pastas na aba lateral direita da tela

Print do outlook com a aba Pastas destacada

2 - Clique no botão de três pontos (...) ao lado do nome da aba "Pastas" e em seguida, selecione a opção "Criar nova pasta".

Imagem do botão de opções das Pastas

3 - Digite o nome da pasta "Outras mensagens" e clique em confirmar.

Com isso você cria uma pasta com o nome "Outras mensagens", mas para esse curso ainda precisamos das pastas "Duvida - FAQ" e "Duvida - Time C", portanto refaça os passos anteriores para a criação dessas outras pastas.

3.2 Excel e conjunto de dados
Temos uma planilha com listas de Pergunta e Respostas Frequentes que você pode baixar por aqui.

Para acessar essa planilha com Make em nosso projeto é necessário que essa planilha esteja salva no Excel Online. Vamos ver como inserir esse arquivo!

1 - Entre com sua conta microsoft no site do Excel.

2 - Na tela inicial busque a opção "Carregar" na barra de ferramentas horizontal.

Print da aba do Excel com destaque par ao botão Carregar na barra de ferramentas

3 - Selecione o arquivo de dados e faça o upload.

Com isso você salva o arquivo em seu onedrive e vai possibilitar o acesso à ele com Make.

E isso é tudo! Vamos lá dar início ao projeto?

https://www.make.com/en

https://www.make.com/en/register

https://www.make.com/en/pricing

https://console.groq.com/keys

https://console.groq.com/keys

https://signup.live.com/signup

https://cdn3.gnarususercontent.com.br/4454-make/Dados%20do%20projeto/Perguntas%20Frequentes%20-%20Bytebank.xlsx

https://www.microsoft.com/pt-br/microsoft-365/excel

@@03
Realizando nossa primeira conexão

Atuamos no setor de comunicação do Banco ByteBank, e nossa tarefa é esclarecer dúvidas dos clientes, auxiliá-los em caso de problemas e melhorar a qualidade da experiência dos clientes com o banco. Para manter esse contato com a clientela, utilizamos telefonemas, mensagens e e-mails. No caso dos e-mails, notamos que recebemos algumas dúvidas que poderiam ser respondidas com uma rápida leitura na nossa cartilha de perguntas e respostas frequentes, o famoso FAQ.

Para otimizar o processo de curadoria das dúvidas e respostas, decidimos construir uma automação capaz de receber os e-mails e identificar se as dúvidas estão relacionadas ao FAQ. Pensamos em um fluxo de construção de automação. Vamos conhecê-lo?

Descrevendo o fluxo de automação
O fluxo começa com a recepção de e-mails, pois precisamos de uma forma dentro da automação para recebê-los. Em seguida, identificamos se o e-mail é uma dúvida ou outra questão que não envolve o FAQ. Se for uma dúvida, verificamos se pode ser respondida pelo FAQ, pois algumas não podem ser respondidas pelas perguntas e respostas frequentes.

Se a dúvida puder ser respondida pelo FAQ, geramos uma resposta de acordo com a cartilha e enviamos um e-mail de resposta aos clientes. Caso o e-mail não seja uma dúvida ou não possa ser respondido pelo FAQ, movemos o e-mail para um suporte mais adequado, normalmente mais humano.

Utilizando a plataforma MAKE e ferramentas necessárias
Para construir esse fluxo, utilizaremos o MAKE como ferramenta-chave, pois é especializada na construção de fluxos de trabalho e permite otimizar processos padronizados e manuais. Além disso, usaremos inteligências artificiais para identificar se o e-mail é uma dúvida e se pode ser respondido pelo FAQ.

Para construirmos esse projeto juntos, é importante ter uma conta no MAKE, na Microsoft e no Grok. Além das contas, é necessário seguir alguns passos relacionados a essas ferramentas, que estão descritos em um tutorial na atividade anterior a este vídeo. Se ainda não conferiu, por favor, faça os passos e depois retorne para construirmos o projeto.

Preparando o ambiente de teste
Já estamos com a conta do Outlook aberta, pois temos um e-mail de um cliente que servirá como teste durante a construção do fluxo de trabalho. O e-mail diz: "Olá, tenho uma dúvida para o banco. Recebi meu bytecard e preciso saber como posso desbloquear o cartão. Aguardo o retorno."

Com o e-mail na caixa de entrada, vamos utilizá-lo na construção do MAKE. Já estamos logados na sessão "My Team", que é a sessão padrão ao entrar no MAKE, onde criaremos nosso cenário. O cenário é um espaço em branco onde podemos adicionar módulos e construir o fluxo.

Criando o cenário no MAKE
Para isso, clicamos no botão roxo no canto superior direito do MAKE, "Create a New Scenario". Ao clicar, começamos a gerar o novo cenário e, na bola central do MAKE, podemos adicionar o primeiro módulo.

O primeiro passo da nossa aplicação é receber e-mails. Para isso, vamos adicionar um módulo que permite receber e-mails lidos. Como nesta aplicação utilizaremos o Outlook, vamos utilizar o módulo do próprio Outlook. Vamos clicar no ícone de adição que aparece no centro da tela. Em seguida, na caixa de pesquisa localizada na parte inferior da nova aba que se abriu, digitamos "Outlook". A primeira opção que aparece é "Microsoft 365 e-mail (Outlook)", que é o módulo que utilizaremos. O módulo é uma forma de se conectar com o processo desejado dentro do nosso fluxo. Dentro desse módulo, há diversas funções disponíveis. Como nosso objetivo é apenas verificar e ler o e-mail que chegou, utilizaremos a função Search Message, que busca por mensagens dentro do Outlook. Vamos clicar nessa função.

Configurando a conexão e coleta de e-mails
Neste ponto, aparece a solicitação para criar uma conexão, que basicamente consiste em fazer o login na conta do Outlook. Vamos criar essa conexão clicando no botão Create Connection. Ele solicita um nome para a conexão, que pode ser alterado, mas deixaremos o padrão. Ao clicar em Save, uma aba para realizar a conexão será exibida. Vamos seguir as instruções fornecidas pelo Make para realizar as conexões e permissões necessárias.

Já temos uma aba para especificar várias informações sobre as mensagens que queremos coletar. A primeira coisa a informar é qual é a pasta principal dos e-mails que desejamos coletar. Vamos clicar no botão Click Here to Choose a Folder e selecionar a caixa de entrada. Assim, faremos uma seleção das primeiras mensagens a serem coletadas, montando uma ordenação de e-mails. Dentro da ordem, selecionaremos a primeira leitura, que é do último e-mail recebido. Para isso, selecionamos Order By, Create, Receive as Dates Time e escolhemos Descending. Dessa forma, o último e-mail recebido será o lido. Definimos o limite de um e-mail, ou seja, faremos a leitura de apenas um.

Limit: 1
Executando o módulo de recepção de e-mails
Vamos salvar e rodar esse módulo para verificar se está funcionando. Clicamos com o botão direito no módulo e selecionamos a opção Run This Module Only, que executará apenas esse módulo.

O módulo traz várias informações sobre o e-mail coletado, mas todas estão contidas dentro de coleções, que são categorias e conjuntos de informações. O que mais nos interessa é o conteúdo da mensagem. Ele fornece uma pré-visualização da mensagem, mas isso pode não ser suficiente dependendo do tamanho do e-mail. Precisamos de todo o corpo da mensagem. Para isso, acessamos Body e depois selecionamos Content, onde temos todo o corpo da mensagem.

1. Body: Content
Convertendo HTML para texto
Observamos que está em HTML. Precisamos enviar esses e-mails para uma IA, que precisa ler o e-mail para verificar se é uma dúvida, um FAQ, etc. Estar em HTML não facilita nosso trabalho, então é importante converter para texto.

Vamos adicionar um novo módulo para converter o HTML em texto. Para isso, clicamos no ícone de adição ao lado do módulo da Microsoft. Selecionamos o TextParser e procuramos a função HTML to Text. Selecionamos essa opção e, dentro do conversor, enviamos o corpo da mensagem em HTML. Já conseguimos ver algumas variáveis relacionadas ao módulo da Microsoft. Buscamos o body, onde encontramos o body, e em seguida a variável content. Deixamos essa configuração e salvamos.

Agora, podemos rodar toda a aplicação clicando em Run Once. Um aviso aparecerá indicando que não é interessante deixar o TextParser como último, mas como é apenas um teste, clicamos em Run Anyway. O resultado é que a saída é apenas o texto da mensagem. Terminamos a primeira etapa do nosso projeto, mas ainda faltam várias outras etapas para concluirmos. Daremos continuidade nos próximos vídeos.

@@04
Identificando dúvidas

Vamos seguir com a construção de todo o nosso fluxo de automação para responder e-mails que podem ser respondidos através da cartilha do FAC. Agora, entramos na etapa em que precisamos identificar se o e-mail recebido é ou não uma dúvida. Isso facilitará muito quando chegarmos na etapa de identificação se essa dúvida pode ser respondida pelo FAC. Portanto, precisamos criar esse "filtro" inicialmente.

Nessa etapa, também precisaremos do suporte de inteligências artificiais. Para isso, utilizaremos o Grok, que é um módulo dentro do Make que podemos utilizar, e que disponibiliza as IAs que a API do Grok também oferece. Além disso, precisamos adicionar alguns filtros e dividir o fluxo de trabalho, pois não é interessante que um e-mail que não seja uma dúvida receba toda a automação e todos os processos que um e-mail de dúvida receberia.

Adicionando o módulo Grok no Make
Vamos ao Make para continuar este projeto. Começaremos adicionando o nosso módulo Grok. Para fazer isso, podemos clicar no botão de mais ao lado do módulo TextFacer. Clicando aqui, abrimos opções para buscar novos módulos, e dentro da barra de pesquisa, selecionaremos Grok. Vamos clicar no módulo e selecionar a função Create a JSON Chart Completion, pois essa função permitirá que a saída do Grok seja um JSON. Isso facilita muito quando selecionamos as variáveis de saída do modelo.

Para definir a estrutura do JSON, utilizamos o seguinte formato:

{ "categoria": "dúvida ou não dúvida" }
COPIAR CÓDIGO
Selecionaremos essa opção, e aqui, da mesma forma que na Microsoft, é solicitada uma conexão. Essa conexão não precisará de e-mail, mas precisará da chave API do Grok, que já ensinamos como coletá-la nas atividades desta aula. Vamos clicar no botão Create a Connection. Será necessário um nome, que pode ser alterado. Em API Key, podemos enviar a chave API. Vamos colar a chave, pois ela já está salva na área de transferência, e clicar em Save. Assim, a conexão será criada.

Configurando o modelo e o prompt do sistema
Com a conexão feita, podemos selecionar o modelo que utilizaremos, clicando na barra do modelo, e selecionaremos o Llama 3.3 70B Versátil. Este é o mais adequado para nossa aplicação. Em seguida, precisamos criar um prompt de sistema, que basicamente indicará qual é o formato JSON da saída deste módulo. Já temos um prompt pronto, que vamos copiar e colar, e ler juntos.

O prompt que utilizaremos é o seguinte:

Você é um assistente de classificação de mensagens do Banco Bytebank. Sua tarefa é ler o conteúdo abaixo e determinar se a mensagem expressa uma dúvida de um cliente ou não. Responda apenas com uma das opções: "dúvida" - se a mensagem contiver uma pergunta de um cliente ou estiver buscando esclarecimento sobre algo do banco. "não dúvida" - se a mensagem for apenas uma afirmação, informação, solicitação direta ou outro tipo de conteúdo.
COPIAR CÓDIGO
Nessa parte, vamos inserir o resultado daquele conversor de HTML para texto, que fizemos no último vídeo, para podermos enviar o texto. O Make já traz a sugestão da variável que podemos inserir. Dentre várias variáveis, selecionaremos o texto do TextFazer. Feito isso, temos todos os prompts prontos e podemos também limitar o máximo de tokens utilizados nessa resposta.

Executando o módulo Grok e criando filtros
Vamos definir o valor 50 para deixar a resposta mais direta e objetiva. Em seguida, clicamos em "Save". Observamos que o módulo do Grok não possui uma saída, ou seja, ele não apresenta os balões que temos no Outlook ou no TextFazer, pois ainda não executamos o Grok. Portanto, ele está sem saída e não temos uma variável associada a ele. Para pensarmos nos filtros ou no fluxo após o Grok, e decidir se é uma dúvida ou não, precisamos executar o módulo para gerar uma saída.

Primeiro, abrimos o TextFazer e copiamos todo o texto. Vamos fazer isso juntos, pois o texto de saída será utilizado. Executamos somente o módulo do Grok clicando com o botão direito e selecionando "Run This Module Only". Ao rodar, ele solicita um texto de entrada, que seria a variável texto. Como estamos rodando apenas este módulo, ele não possui essa variável. Colamos o texto copiado e clicamos em "OK". Assim, ele executa a entrada e, ao clicar em "Mais" ao lado de "Result", vemos o resultado: a categoria foi identificada como dúvida.

Criando rotas e filtros para e-mails
Com isso, podemos criar um fluxo que separa os casos em que o e-mail é uma dúvida ou não. Para isso, criamos uma rota que divide o fluxo dentro do nosso sistema. Na rota, podemos clicar no botão de "Flow Control" na barra inferior ou adicionar outro elemento clicando em "Mais". Selecionamos a função "Router" para dividir a rota. Conectamos a linha do Grok à rota e clicamos na rota para gerar duas opções.

Na primeira opção, montamos o caso em que o resultado do Grok não é uma dúvida. Adicionamos um filtro nesse caminho, clicando na ligação e criando uma condição. A condição é: se o resultado do Grok na categoria for igual a "não dúvida", salvamos. Com o primeiro filtro, podemos mover o e-mail para outra categoria no Outlook, facilitando a busca e entendimento dos e-mails recebidos. Para isso, clicamos em "Mais" no módulo do primeiro caminho, selecionamos o Microsoft Outlook e escolhemos a opção "Move a Message". Podemos mover uma mensagem para qualquer pasta desejada, utilizando o ID de mensagem coletado ao executar o módulo da Microsoft. Definimos a mensagem e a movemos para a pasta "Outras mensagens". Salvamos e concluímos essa parte.

Finalizando a configuração dos filtros
Criamos um novo filtro para o caso de uma dúvida. A condição será que a categoria, resultado dado pelo Grok, seja igual a "dúvida". Salvamos e temos todos os filtros de rota, incluindo o primeiro caminho dentro do fluxo. Com isso, construímos a segunda etapa, que é a identificação de uma dúvida. Adicionamos um anexo para que, caso não seja uma dúvida, o e-mail seja colocado em uma pasta relacionada a outras mensagens. Ainda falta identificar se o e-mail pode ser respondido pelo FAQ, o que faremos no próximo vídeo.

@@05
Associando dúvida ao FAQ

A primeira parte da categorização dos e-mails que recebemos já foi realizada, que foi identificar se o e-mail enviado por uma pessoa cliente é ou não uma dúvida. Agora, precisamos fazer uma segunda verificação: se essa dúvida identificada pode ou não ser respondida através das informações do nosso FAQ.

Para responder a essa dúvida, utilizaremos outra inteligência especial, outro uso do nosso GROC, no qual precisaremos informar tanto o conteúdo do nosso FAQ quanto a mensagem da pessoa cliente. Vamos ao nosso Make para construir essa automação.

Continuando o projeto e configurando o Excel
Voltando ao nosso projeto, continuamos a partir da nossa rota. Já fizemos o primeiro caminho da nossa rota, que seria o caso em que o e-mail não fosse uma dúvida, e apenas o movemos de categoria. Agora, vamos trabalhar com o segundo caminho da nossa rota, que é o caso em que o e-mail é uma dúvida. Nosso objetivo é informar o FAQ e o e-mail da pessoa cliente para uma IA.

Pensando no fluxo até chegar à IA que fará essa análise, precisamos primeiro ter nosso FAQ e coletar as informações de dentro dele. Nos materiais desta aula, já disponibilizamos toda a planilha das perguntas, respostas e perguntas frequentes dentro do ByteBank, e também ensinamos como inserir isso na sua conta do Excel, utilizando o Microsoft, que é a ferramenta que utilizaremos aqui.

Coletando dados do FAQ com o Excel
A partir do Make, faremos a coleta de todas as perguntas e respostas dessa planilha. Para isso, utilizaremos o módulo do Excel. Vamos clicar na bolinha do segundo caminho da rota, pois vamos adicionar o Excel. Digitamos na barra de pesquisa e acessamos o módulo do Excel. Como queremos fazer a leitura dos valores dentro de uma planilha, a função que escolheremos é List Worksheet Rows, que basicamente lista as linhas dentro de uma planilha. Selecionamos essa função.

List Worksheet Rows
COPIAR CÓDIGO
A conexão que fazemos no Excel é a mesma que utilizamos na Microsoft, com a mesma conta. Selecionamos o método de consulta e encontramos a planilha. Deixamos a opção "Select from the List", pois isso nos direciona diretamente para o Drive onde está a planilha, mas também poderíamos utilizar um e-mail.

Connection: My Microsoft connection (...)
Select a method: Select from the list
Choose your OneDrive location: My Drive
COPIAR CÓDIGO
Selecionando e processando a planilha
Selecionamos do Drive e, dentro do Workbook, que seria o nome do arquivo, clicamos no botão "Click Here to Choose a File". Esperamos um pouco, pois ele irá buscar no Outlook, e selecionamos nossa planilha, "Perguntas Frequentes ByteBank".

Workbook* : / Perguntas Frequentes - Bytebank.xlsx
COPIAR CÓDIGO
Não nos esquecemos de selecionar qual planilha faremos a leitura, que seria o Worksheet. Selecionamos a planilha 1, deixamos a opção de pular as linhas após uma linha em branco selecionada, e removemos o limite de linhas a serem coletadas.

Worksheet*: Planilha1
Limit: 
COPIAR CÓDIGO
Salvamos e rodamos a aplicação para verificar se a coleta está correta. Clicamos com o botão direito em "Rounded Model Only". Ele roda rapidamente, e verificamos que há um Input, mas não precisamos nos preocupar, e há um Output. Conseguimos ver que há diversos bundles, como se fossem conjuntos de informações, ou cada operação que ele rodou. Dentro de cada um desses bundles, conseguimos ver as linhas e as respostas, o texto de cada uma dessas linhas, tanto na linha 1, em seguida, a linha 2, e assim por diante.

Agregando textos com o Text Aggregator
Fechamos essa parte, pois é importante termos essa noção. Não conseguimos enviar um texto completo, da forma como está, para uma API, um texto do nosso FAQ. Do jeito que está, separado em bundles, nessas diversas coleções, não será possível enviar de maneira adequada ou mais simples para nossa IA todo o texto do FAQ. Precisaremos, de alguma forma, agregar todos os textos desse bundle em um único texto e, assim, enviá-lo para nossa IA.

O Make já dispõe de ferramentas capazes de construir essa agregação. A ferramenta é bem intuitiva e se chama Text Aggregator. Conseguimos acessá-la dentro dos tools do Make, que podemos acessar na barra inferior, em tools. É o ícone vermelho, ou então, clicando no mais, digitamos na barra de pesquisa tools. Para facilitar, selecionamos o botão de tools. A função das ferramentas que pegaremos será, lá embaixo, o Text Aggregator.

Text aggregator
COPIAR CÓDIGO
Configurando o Text Aggregator
Vamos selecionar o módulo, conectar diretamente com o Excel e, em seguida, configurá-lo. No Source Module, especificamos qual módulo buscará as variáveis para agregar o texto. Aqui, utilizamos o Excel.

Source Module*: Microsoft 365 Excel - List Worksheet Rows [6]
COPIAR CÓDIGO
Ele solicita que especifiquemos o texto a ser inserido. Para o texto, colocamos "Pergunta:". Em seguida, acessamos a seção de variáveis do Microsoft Excel, separamos e selecionamos a variável Text em "Perguntas". Após "Pergunta:", inserimos um "Enter" e adicionamos "Resposta:". Colocamos um espaço e, então, selecionamos a variável Respostas para o texto.

Text: Pergunta: 
Text: Pergunta: 6. Row: (A): Perguntas: Text
Resposta:
Text: Pergunta: 6. Row: (A): Perguntas: Text
Resposta: 6. Row: (B): Respostas: Text
COPIAR CÓDIGO
Finalizando a configuração do Text Aggregator
Após isso, habilitamos a opção "Show Advanced Settings", pois desejamos que todas as perguntas e respostas sejam separadas por uma quebra de linha. Definimos um "Row Separator" como "New Row", para que ele pule a linha.

Row separator: New row
COPIAR CÓDIGO
Salvamos e, agora, temos nosso texto completo do FAQ criado.

Integrando o Grok para análise de dúvidas
Podemos adicionar novamente o Grok dentro do módulo. Clicamos no botão de adicionar, após os Tools, e inserimos o Grok, a função de JSON. Selecionamos novamente o modelo, que é o Llama 3.3, especificamente o 3.3 70B versátil.

Create a JSON Chat Completion
Model*: llama-3.3-70b-versatile
COPIAR CÓDIGO
No System Prompt, já temos um Prompt salvo, similar ao que utilizamos anteriormente. O JSON deve ter a seguinte estrutura: resposta categoria, que pode ser "dúvida FAQ" ou "dúvida-time C", indicando se a dúvida pode ser respondida pelo FAQ ou se requer suporte humano.

System Prompt*
O JSON deve ter a seguinte estrutura:

{
    "categoria": "dúvida FAQ ou dúvida - time C"
}
COPIAR CÓDIGO
Configurando a mensagem do usuário e executando o Grok
Na mensagem de usuário, também temos um Prompt salvo. A tarefa é verificar se a dúvida pode ser respondida com base no FAQ fornecido. Responda apenas com "dúvida FAQ" se a dúvida puder ser respondida usando o FAQ, ou "dúvida-time C" se exigir suporte humano. Informamos a variável de texto do Tools que criamos e adicionamos outro texto: "Aqui está o conteúdo da mensagem recebida", que é a mensagem do usuário.

User Message*

Você é um assistente que analisa dúvidas de clientes.
Sua tarefa é verificar se a dúvida pode ser respondida com base em um FAQ fornecido.
Responda apenas com:

"dúvida FAQ" - se a dúvida pode ser respondida usando o conteúdo do FAQ.
"dúvida - time C" - se a dúvida não pode ser respondida pelo FAQ e exige suporte humano.
Use apenas uma dessas duas respostas.

Aqui está o conteúdo de referência do FAQ:
7. text

Aqui está o conteúdo da mensagem recebida:
2. Text
COPIAR CÓDIGO
No modo HTML, inserimos o texto de HTML. Definimos o limite de 80 tokens e salvamos o Grok.

Max tokens returned: 80
COPIAR CÓDIGO
Executamos o Grok para verificar se está funcionando corretamente. Precisamos passar a mensagem do usuário e o que a ferramenta de Tools enviou. A mensagem do usuário já foi copiada anteriormente, então apenas colamos aqui. Por fim, ele solicita a mensagem da ferramenta de Tools. Copiamos a primeira linha do Excel e inserimos, podendo ser qualquer texto, apenas para executar o Grok. Após isso, ele gera uma saída, provavelmente "dúvida-time C", pois não contempla, mas já temos uma saída.

Dividindo o fluxo com flow control
Com a saída gerada, podemos dividir o fluxo novamente. Utilizamos o flow control para separar as rotas, pois agora teremos duas novas saídas: a pergunta que pode ser respondida pelo FAQ e a que exigirá suporte humano.

Router
COPIAR CÓDIGO
A primeira saída deixamos em espera, enquanto a segunda será a "dúvida-time C". Clicamos na rota para gerar o filtro, cuja condição é que o resultado do Grok, na parte de categoria, seja igual a "dúvida-time C".

Condition: 9. result: categoria
Text operators: Equal to
dúvida - time C
COPIAR CÓDIGO
Movendo e-mails para a categoria correta
Salvamos o filtro e, nesse caso, movemos o e-mail enviado pelo cliente para a categoria no Outlook destinada ao time C. Clicamos em adicionar, selecionamos Microsoft Outlook e utilizamos a função "move a message".

Move a Message
Message ID*: 1. Message ID
Mail Folder*: / Duvida - Time C
COPIAR CÓDIGO
Selecionamos o message ID e a pasta de destino será "dúvida-time C". Salvamos e, assim, construímos a primeira opção de rota para o caso em que a pergunta não pode ser respondida pelo FAQ.

Ainda falta a etapa em que a dúvida enviada no e-mail possa ser respondida pelo FAQ. Essa parte será concluída no próximo vídeo.

@@06
Finalizando a automação

Falta apenas uma etapa para concluirmos todo o fluxo que construímos até aqui. Essa etapa envolve a criação da resposta para a pergunta, alinhada com nosso FAQ, e a elaboração do e-mail que será enviado para a pessoa, solucionando sua dúvida. É importante saber que podemos utilizar inteligências artificiais nessa etapa também, pois, se identificarmos que é uma dúvida que pode ser respondida através do FAQ, a IA conseguirá estruturar a solução da resposta com base na cartilha do FAQ.

Podemos utilizar essas IAs e também os módulos do Outlook para a construção e envio do e-mail. Como vamos construir esse fluxo? Vamos para o nosso make para dar continuidade e finalizar nosso projeto.

Adicionando filtros e configurando o grok
Até agora, criamos uma parte do fluxo final, que foi mover o e-mail para a categoria de dúvidas do "time C", para obter apoio humano para perguntas que não podem ser resolvidas pelo FAQ. Agora, vamos para a parte em que o e-mail pode ser respondido pelo FAQ. A primeira coisa a fazer é adicionar o filtro, pois uma pergunta que precisa do "time C" não pode passar por todo o processo de resposta do FAQ. Vamos clicar na rota para criar um filtro. Esse filtro será a saída do nosso grok, que é a categoria, e precisa ser igual à dúvida FAQ. Vamos salvá-lo e adicionar um novo grok, que será a IA que gerará essa resposta.

Vamos clicar no botão para adicionar um módulo e selecionar o grok. A função que utilizaremos será a mesma que estamos usando até agora, que é a do JSON. Dentro dela, vamos selecionar o modelo, como o Llama 3.3, que é o mesmo que estamos utilizando, versão 3.3 70B versátil.

llama-3.3-70b-versatile
COPIAR CÓDIGO
Estruturando a resposta com HTML
No prompt, já deixamos tudo preparado. Vamos copiar, apagar e colar: "Seu JSON deve ter esta estrutura: {texto: 'texto de resposta'}", que será a resposta gerada pelo próprio grok.

{
    "Texto": "texto de resposta"
}
COPIAR CÓDIGO
Dentro da mensagem, vamos copiar nosso prompt: "Você é um assistente virtual do banco Whitebank. Sua tarefa é redigir uma resposta educada e clara para a dúvida de um cliente, com base no FAQ fornecido. Siga esta estrutura obrigatória na resposta: 1. Agradecimento pela dúvida enviada, exemplo: 'Obrigado por entrar em contato com o banco Whitebank.' 2. Resposta à dúvida do cliente com base no conteúdo do FAQ, de forma direta e cordial. 3. Encerramento simpático, informando que o FAQ está disponível para mais informações e que o banco está à disposição para outras dúvidas." Essa é a estrutura do e-mail. Devemos ser cordiais, manter a linguagem formal e clara.

Você é um assistente virtual do Banco Bytebank. Sua tarefa é redigir uma resposta educada e clara para a dúvida de um cliente, com base em um FAQ fornecido.
Siga esta estrutura obrigatória na resposta:

1. Agradecimento pela dúvida enviada (ex: "Obrigado por entrar em contato com o Banco Bytebank.")
2. Resposta à dúvida do cliente com base no conteúdo do FAQ, de forma direta e cordial.
3. Encerramento simpático, informando que o FAQ está disponível para mais informações e que o banco está à disposição para outras dúvidas.

Seja cordial, mantenha a linguagem formal e clara. Use de HTML para manter a formatação adequada do texto.
COPIAR CÓDIGO
Um detalhe importante é usar HTML para manter a formatação adequada do texto. Isso é um pedido do próprio módulo do Outlook, pois, ao estruturar um texto para o e-mail, é necessário que esteja em HTML, senão a mensagem ficará sem formatação. Portanto, pedimos que a saída esteja estruturada em HTML.

Executando o grok e criando o rascunho do e-mail
Abaixo estão as informações de referência. Vamos colocar nosso FAQ, que estará no resultado dos tools de texto, e também a mensagem do cliente, que está em textface. O máximo de tokens que vamos colocar será 500, o que é adequado para uma mensagem. Vamos salvar.

500
COPIAR CÓDIGO
Desenvolvemos nosso grok. Vamos executá-lo para obter uma resposta. Antes de executar, vamos clicar com o botão direito e selecionar "Run this module only". Vamos adicionar tanto o texto do FAQ quanto a mensagem do cliente. Na parte de tools, texto agregado, colocamos as informações do FAQ. Aqui está a primeira linha da planilha do nosso FAQ, que copiamos e colamos. Na parte do HTML, do textface, adicionamos o texto da pessoa que enviou a mensagem. Clicamos em OK, o grok roda e já gera um resultado. Vemos algumas estruturas em HTML, tudo parece estar indo bem.

Agora, vamos adicionar um módulo que criará o e-mail a ser enviado para essa pessoa.

Estruturando o envio do e-mail e organizando mensagens
Dentro do Make, com o Outlook, conseguimos criar o e-mail e enviá-lo diretamente para a pessoa. No entanto, neste caso específico, não faremos isso, pois estamos trabalhando com IaaS, uma automação nova, e é importante que revisemos o texto para garantir que não há erros. Portanto, vamos criar um rascunho que estará totalmente estruturado, pronto para ser enviado após revisão.

Para isso, clicaremos no botão de mais, ao lado do grok, para adicionar o módulo da Microsoft. Este módulo, que vamos adicionar, está mais abaixo, chamado Create Address Message. Ele criará uma mensagem que será um rascunho. O Subject, que seria o assunto, pode ser definido como "RE", indicando uma resposta.

RE: 
COPIAR CÓDIGO
Vamos descer até a parte da Microsoft, onde podemos encontrar o assunto da dúvida original. Assim, "RE" será a resposta ao assunto enviado.

RE: 1. Subject
COPIAR CÓDIGO
Dentro do Body Content, que é a mensagem a ser enviada, podemos clicar e selecionar o resultado do nosso grok, que é o texto criado. Não precisamos definir a importância, mas precisamos adicionar as pessoas que receberão o e-mail. Vamos adicionar um item, onde podemos informar tanto o endereço de e-mail quanto o nome da pessoa. Ao adicionar o e-mail, utilizaremos o mesmo e-mail enviado pela pessoa que nos enviou a dúvida, que o módulo da Microsoft nos fornece. Na parte de Sender, em e-mail address, veremos tanto o endereço quanto o nome da pessoa. Selecionaremos o botão Address para colocar o endereço de e-mail e, no nome, selecionamos a variável Name.

1. Sender: Email Address: Address
1. Sender: Email Address: Name
COPIAR CÓDIGO
Finalizando o fluxo e verificando resultados
Feito isso, estruturamos todo o nosso rascunho. Vamos clicar em Salvar e, por fim, mover o e-mail original enviado pelo cliente para uma pasta chamada "Dúvidas FAQ", para ficar mais organizado e fácil de encontrar. Adicionaremos outro módulo, também do Outlook, chamado Move a Message. Na parte de Message ID, já sabemos como proceder. Vamos ao primeiro módulo da Microsoft e selecionamos o Message ID. A pasta que selecionaremos será "dúvida-FAQ".

1. Message ID
/ Duvida - FAQ
COPIAR CÓDIGO
Salvar e pronto!

Agora temos todo o nosso fluxo pronto. Vamos clicar no botão Run on para executar uma vez e verificar o resultado. Ao clicar, ele executará tudo, e podemos observar para onde os fluxos estão indo. Vamos conferir no e-mail se deu certo. Na Caixa de Entrada, o e-mail já não está mais lá. Vamos verificar se ele foi para "dúvida-FAQ". O mesmo e-mail já está na parte de "dúvida-FAQ". Nos rascunhos, já temos a criação dos nossos rascunhos. Vamos conferir? Já temos para quem enviar, o assunto, que é a resposta, e a mensagem de agradecimento por entrar em contato. Para desbloquear a caixa de entrada, a pessoa pode seguir os passos indicados. Esses passos estão de acordo com nossa planilha, na linha 9, e a resposta está adequada, inclusive consultando nosso FAQ.

Agendando execuções automáticas
Conseguimos ver que está funcionando adequadamente. Voltando ao Make, como estamos trabalhando no banco e verificando que a integração está funcionando, podemos agendar quantas vezes ele pode rodar ou em que momentos essa aplicação pode rodar, clicando no botão Every 15 Minutes. Podemos, ao clicar nele, habilitar um agendamento, definindo intervalos e horários adequados para as operações.

Run scenario: At regular intervals
Minutes: 15
COPIAR CÓDIGO
Porém, saindo um pouco do projeto, como é mais comum em estudos, não recomendamos ativar isso para não consumir as operações gratuitas, caso a conta seja gratuita. No entanto, é possível utilizar e deixar rodando de forma automática. Com isso, já vimos que nosso projeto funciona, organiza todos os e-mails, gera uma resposta que pode ser enviada e verificada, e funciona muito bem.

@@07
Para saber mais: Limitando tokens

Durante o uso do módulo de IA, definimos um máximo de tokens de retorno. Mas afinal o que são os tokens?
Tokens equivalem a uma unidade de texto, podendo ser uma palavra, partes de uma palavra ou sinais de pontuação. Como exemplo, a palavra “não” pode corresponder a 1 token, mas a palavra “dúvida” pode contabilizar 2 tokens ou mais!

A quantidade de tokens pode variar a depender do provedor da LLM e o do modelo LLM escolhido. Colocamos nesse site a frase “não dúvida” para calcular a quantidade de tokens usados e seus custos. Como resultado obtemos 5 tokens criados utilizando o Groq e o modelo llama-3.3-70b-versatile.

Dica: você pode consultar o mesmo site para fazer outros testes e estimar as saídas de suas aplicações!
Sabendo disso, é esperado que a quantidade de tokens das saídas do Groq na aplicação do Make pode fique próximo ao valor de cinco, mas é importante sempre definir um limite de tokens para evitar gastos desnecessários caso o prompt não seja eficiente.

Essa medida se torna ainda mais necessária quando utilizamos de APIs pagas em nosso projeto. Não é o caso desse curso, mas é válido lembrar dessa prática pois evita maiores prejuízos, caso o projeto execute de um modo além do esperado.

https://unstract.com/tools/llm-token-counter/

https://unstract.com/tools/llm-token-counter/

@@08
Para saber mais: Utilizando serviços Gmail

No projeto deste curso, iremos utilizar a conta da Microsoft para construir a aplicação. Mas sabemos que o Google também oferece serviços similares aos da Microsoft e, dependendo do seu contexto, pode fazer mais sentido utilizar as aplicações do Gmail.
A conexão da conta Google com o Make pode ser um menos intuitiva, visto que depende muito da característica da conta. Pensando nisso, montamos esse tutorial para facilitar a criação da conexão entre sua conta Gmail e a plataforma do Make para caso você queira utilizar esse serviço em seus projetos.

Esse tutorial foi construído com base no tutorial do próprio Make, se preferir, confira ele nesse link.
Pré-requisito
Para conectar uma conta do Gmail ao Make, você precisa ter uma conta Google ativa (como fulano@gmail.com). Se ainda não tiver, crie uma gratuitamente aqui.

Sobre os tipos de conexão no Make
Existem dois jeitos diferentes de conectar o Gmail ao Make, dependendo do tipo de conta e permissões que você tem:

Opção 1 - Usando credenciais fornecidas pelo Make

Essa opção é válida apenas para empresas que:

Têm uma assinatura paga da Google Cloud Platform;
Usam um e-mail com domínio personalizado, como nome@suaempresa.com.
Se esse for o seu caso, você pode ir direto para o final deste guia, na parte chamada “Crie uma conexão no Make”, e pular os passos de criação de projeto.

Opção 2 - Usando suas próprias credenciais (mais comum)

Essa é a opção usada pela maioria das pessoas que têm uma conta normal do Gmail (como @gmail.com ou @googlemail.com). Você vai seguir este caminho se:

Usa uma conta gratuita do Gmail;
Ou tem uma conta paga do Google, mas quer mais controle sobre o que o Make pode fazer com seu Gmail.
Nesse caso, como você não pode usar as credenciais padrão do Make, vai precisar criar suas próprias credenciais no Google Cloud Platform.

Obs: Para isso, será necessário ativar permissões no seu projeto. Uma delas se chama serviceusage.services.enable.
Se você não tiver permissão ativar isso sozinho, será preciso pedir ajuda a quem é dono do projeto ou tem permissão de administrador (IAM) no Google Cloud.
Agora que você já entendeu qual tipo de conexão vai usar, siga para o próximo tópico:

Como criar e configurar um projeto no Google Cloud Platform para usar com o Gmail
Se você está usando um e-mail que termina com @gmail.com ou @googlemail.com, vai precisar criar um projeto no Google Cloud Platform (GCP). Esse projeto é necessário para permitir que o Make acesse sua conta do Gmail com segurança.

Vamos ao passo a passo:

Passo 1 - Acesse o Google Cloud Platform
Acesse o site do Google Cloud Platform (GCP) e entre com sua conta do Google (a mesma do Gmail que você quer conectar ao Make).

Passo 2 - Crie um novo projeto
Ao entrar na plataforma, você verá uma página de boas-vindas.
Clique em “Selecionar projeto” (no topo da tela) e depois em “Novo projeto”, no canto superior direito. Outra opção, é utilizar a barra superior de pesquisa e digitar “Criar um projeto”, então selecione a primeira opção.
Alt text: A imagem mostra a interface do Google Cloud Platform com a barra de pesquisa ativa, onde foi digitado “criar um projeto”. O primeiro resultado da busca, destacado com um contorno vermelho, é a opção “Criar um projeto” na seção IAM e administrador.

Dê um nome para o projeto (pode ser qualquer nome que ajude você a identificá-lo).
Alt text: A imagem mostra a tela de criação de um novo projeto no Google Cloud Platform. O campo "Nome do projeto" está preenchido com “projeto-make-456818” e o ID do projeto é exibido logo abaixo, com a observação de que não poderá ser alterado. O campo "Local" está definido como "Sem organização". Na parte inferior, há dois botões: “Criar” em azul e “Cancelar” em cinza.

Em “Local”, você pode deixar o que já estiver preenchido ou escolher uma organização, se tiver.
Se não aparecer nada, tudo bem — continue assim mesmo.
Clique em Criar.
Passo 3 - Confirme se o projeto está selecionado
Depois que o projeto for criado:

No menu superior, clique novamente em “Selecionar projeto”.
Verifique se o nome do projeto que você criou está selecionado. Se não estiver, clique nele para ativá-lo.
Ative a API do Gmail (se ainda não tiver feito)
Se ainda não ativou a API do Gmail no seu projeto, siga os passos abaixo:

1 - Na barra de pesquisa superior do Google Cloud Platform, digite “APIs e serviços”.

Alt text: A imagem mostra a barra de pesquisa do Google Cloud Platform com o termo “apis e serviços” digitado. O primeiro resultado exibido, destacado com um contorno vermelho, é “APIs e serviços” com a descrição “Gerencie APIs para serviços em nuvem”.

2 - No menu lateral selecione “Biblioteca”.

3 - Na barra de busca que aparece no topo da tela, digite: Gmail API e tecle Enter.

Alt text: A imagem mostra a página da Biblioteca de APIs do Google Cloud Platform com a busca “Gmail API” realizada. Há um resultado visível, sendo o primeiro a “Gmail API” da categoria Google Enterprise API, acompanhado do ícone do Gmail e de uma breve descrição em inglês sobre suas funcionalidades, como visualizar e gerenciar dados da caixa de entrada.

4 - Clique no resultado Gmail API (ele tem o ícone do Gmail com um envelope vermelho).

5 - Clique em Ativar.

Se aparecer o botão “Gerenciar” em vez de “Ativar”, isso significa que a API já está habilitada. Nesse caso, você pode seguir para o próximo passo.
Configure a tela de consentimento do OAuth (OAuth consent screen)
Agora, você vai configurar a “tela de consentimento”. Essa é a parte em que o Google mostra para você (ou outros usuários) quais permissões o aplicativo vai solicitar ao acessar a conta do Gmail.

Siga o passo a passo:

1 - Na barra de pesquisa superior digite “Google Auth Platform”.

Alt text: A imagem mostra a barra de pesquisa do Google Cloud Platform com o termo “Google Auth Platform” digitado. O primeiro resultado exibido, destacado com um contorno vermelho, é “Google Auth Platform” com a descrição “Configuração e credenciais do OAuth”.

2 - Clique em “Vamos começar” (Get Started).

3 - Em Informações do app (Overview > App information):

No campo Nome do app, escreva: Make
No campo de e-mail do desenvolvedor, coloque seu endereço do Gmail
Clique em Próxima (Next)
4 - Em Público-alvo (Audience):

Selecione Externo (External)
Clique em Próxima (Next)
Esse é o tipo certo para quem vai usar o app com uma conta @gmail.com.
5 - Em Informações de contato (Contact Information):

Coloque novamente seu e-mail do Gmail
Clique em Próxima (Next)
6 - Em Finalização (Finish):

Marque a opção aceitando a Política de dados do usuário do Google
Clique em Continuar > Criar (Continue > Create)
7 - Em Branding (Marca):

No campo Domínios autorizados (Authorized domains), adicione: make.com e integromat.com
Clique em Salvar (Save)
Alt text: A imagem mostra a seção “Branding” do Google Cloud Platform, onde é possível configurar os domínios autorizados para uso com OAuth. Os campos exibem os domínios “make.com” e “integromat.com” como autorizados. Há também um botão “+ Adicionar domínio” e informações sobre a necessidade de verificação dos domínios via Google Search Console. No menu lateral, estão visíveis as opções Visão geral, Branding, Público-alvo, Clientes, Acesso a dados e Central de verificação.

8 - Em Público-alvo (Audience):

Clique em Test users e adicione seu próprio e-mail do Gmail
Clique em Salvar e continuar
Isso mantém o projeto no modo de testes, o que é ideal durante a configuração.
9 - Em Acesso aos dados (Data Access):

Clique em Adicionar ou remover escopos (Add or remove scopes)
Adicione os seguintes dois escopos:
https://www.googleapis.com/auth/userinfo.email
https://mail.google.com
COPIAR CÓDIGO
Você pode colar esses links diretamente em Adicionar escopos manualmente ou usar a tabela com filtros
Clique em Atualizar (Update)
10 - Clique em Salvar (Save) para finalizar essa etapa.

Sobre o status de publicação do seu projeto
Depois de configurar a tela de consentimento, o seu projeto ficará, por padrão, com o status "Em teste" (Testing). Isso funciona, mas tem uma limitação importante.

O modo padrão após criar o projeto é o ”Em teste”, ele funciona normalmente no Make. Porém, você vai precisar autorizar novamente a conexão a cada semana.

No modo In production (Em produção), você não precisa autorizar a conexão toda semana. Para ativar, vá até Google Auth Platform > Seção Público-alvo (Audience) > Clique em “Publicar app (Publish app)”.

Atenção: Ao publicar o app, pode aparecer um aviso “Needs verification” (Precisa de verificação).
Isso significa que o Google quer que seu app passe por um processo de verificação de segurança.

Você pode ignorar isso por enquanto, já que o Make ainda permite a conexão com apps não verificados. Mas não há garantia de que o Google continuará permitindo isso no futuro. Para mais detalhes, você pode consultar a documentação oficial do Google sobre o status de publicação.

Crie suas credenciais do cliente OAuth (Client Credentials)
Agora que sua tela de consentimento já está configurada, é hora de gerar as credenciais que o Make vai usar para se conectar ao seu Gmail com segurança.

Siga os passos:

1 - No menu lateral do Google Auth Platform, clique em “Clientes” (Clients).

2 - Clique no botão “+ Criar cliente” (Create Client).

Alt text: A imagem mostra a seção “Clientes” da plataforma Google Auth Platform, onde são gerenciados os clientes OAuth 2.0. No topo da página, há um botão destacado “+ Criar cliente”, seguido das opções “Excluir” e “Restaurar clientes OAuth excluídos”.

3 - No campo Tipo de aplicativo (Application type), selecione: Aplicativo da Web (Web application)

No campo Nome, dê um nome para o cliente OAuth. Pode ser algo como Gmail Make, só para você identificar depois.
Em URIs de redirecionamento autorizados (Authorized redirect URIs):
Clique em “+ Adicionar URI”
Cole o seguinte link:
https://www.integromat.com/oauth/cb/google-restricted
COPIAR CÓDIGO
Clique em Criar (Create).
Depois de criado, verifique o pop-out que apareceu, ou acesse a tabela IDs do cliente OAuth 2.0 que você acabou de gerar.
Copie os dois valores que aparecerem:
ID do cliente (Client ID)
Chave secreta do cliente (Client Secret)
Alt text: A imagem mostra a confirmação de criação de um cliente OAuth no Google Cloud Platform. São exibidos os campos “ID do cliente” e “Chave secreta do cliente”, ambos com os valores parcialmente ocultos. Abaixo, constam a data de criação, o status “Ativadas” com um ícone verde e a opção para “Baixar o JSON”. Também há um aviso de que o acesso OAuth é restrito a usuários de teste listados na tela de consentimento do OAuth.

Guarde essas informações em um local seguro. Você vai usá-las no Make, nos campos Client ID e Client Secret.

Crie uma conexão no Make
Agora que você já tem o ID do cliente e a Chave secreta do cliente criados no Google Cloud, vamos finalmente conectar sua conta Gmail ao Make.

Siga os passos:

1 - Acesse sua conta no Make (antigo Integromat).

2 - Crie um novo cenário (scenario) ou abra um já existente.

3 - Adicione um módulo do Gmail ao cenário.

4 - Clique em “Create a connection” (Criar uma conexão).

5 - (Opcional) No campo Nome da conexão (Connection name), você pode escrever um nome para identificar essa conexão. Exemplo: Minha Conta Gmail

Atenção: Para contas que usam email com final @gmail.com ou @googlemail.com, o Make pode pedir as credenciais personalizadas.
Se for o caso, ative a opção “Mostrar configurações avançadas (Show advanced settings)”
Cole o ID do cliente e a Chave secreta do cliente que você criou na Google Cloud Platform
Alt text: A imagem mostra a tela de criação de uma conexão no serviço Make, com o nome da conexão preenchido como “Minha conta Gmail GCP”. Estão visíveis os campos “Client ID” e “Client Secret”, ambos preenchidos, além de um botão roxo ativado com a opção “Show advanced settings” e, ao lado do botão “Close”, encontra-se o botão “Sign in with Google” para autenticação.

Clique em “Sign in with Google” (Entrar com o Google)
Faça login com sua conta do Gmail (a mesma usada no projeto da Google Cloud)
Permita todos os acessos solicitados e confirme
E pronto! Sua conta do Gmail está conectada ao Make!

Agora você já pode usar os módulos do Gmail nos seus cenários para enviar, ler ou organizar e-mails automaticamente.

Se quiser editar ou remover essa conexão no futuro, vá até a aba Conexões (Connections) no menu principal do Make.

https://apps.make.com/google-email

https://myaccount.google.com/

https://console.cloud.google.com/

https://support.google.com/cloud/answer/10311615#zippy=

https://www.integromat.com/oauth/cb/google-restricted

https://www.make.com/

https://support.google.com/cloud/answer/10311615#zippy=

https://www.integromat.com/oauth/cb/google-restricted

https://www.make.com/

@@09
Para saber mais: Entendendo a barra de ferramentas do Make

Quando estamos montando nosso projeto no Make é possível ver uma barra na parte inferior do cenário:
Alt text: A imagem mostra a barra de controle de execução de um cenário na plataforma Make. À esquerda, há um botão roxo “Run once” para executar o fluxo uma vez, seguido de um botão desativado indicando execução a cada 15 minutos. À direita, há diversos ícones para salvar, exibir variáveis, configurações, notas, versões anteriores, auto-alinhamento e opções adicionais, além de três blocos coloridos para módulos específicos do Make e um botão “+” para adicionar novos módulos.

Essa barra fornece botões que são bem úteis para testar, configurar e gerenciar seu cenário. Vamos conhecer cada um deles?

Para a explicação, seguiremos a ordem da esquerda para direita na organização de cada botão.

Run once - Execute uma vez
Executa o cenário uma única vez manualmente. Muito usado para testar se o fluxo está funcionando como esperado ou para obter saídas desejadas.

Every 15 minutes - Agendamento
Nessa opção é possível configurar quando e com que frequência um cenário será executado automaticamente.

Alt text: A imagem mostra a janela de configurações de agendamento do Make. O cenário está configurado para ser executado em intervalos regulares de 15 minutos, valor mínimo permitido. Há também uma seção de agendamento avançado, onde é possível adicionar um item. Na parte inferior, há a opção “Show advanced settings” desativada, e os botões “Cancel” e “Save” para cancelar ou salvar as configurações.

Dentro desse painel, você pode escolher como e quando o cenário será executado. Veja as opções:

Opção	O que faz
Immediately	Executa o cenário assim que um gatilho é ativado (disponível apenas para alguns tipos de gatilhos).
At regular intervals	Executa o cenário repetidamente com o intervalo que você definir (ex: a cada 10, 30 ou 60 minutos).
Once	Executa o cenário uma única vez em uma data e hora específicas.
Every day	Executa todos os dias, no horário que você escolher.
Days of the week	Executa apenas em dias específicos da semana (ex: segunda e quarta).
Days of the month	Executa em dias específicos do mês (ex: dia 1, 15 e 30).
Specified dates	Executa apenas em datas específicas (ex: 01/05, 25/12).
On demand	O cenário só será executado manualmente ou por chamada via API. Ideal para testes ou execuções pontuais.
A frequência mínima entre execuções pode variar de acordo com o seu plano no Make (gratuito ou pago).
Se quiser que o cenário funcione só por um período específico, você pode:

Marcar a opção “Show advanced settings” (Mostrar configurações avançadas).
Informar a data de início (Start) e a data de término (End) da execução automática.
Dica extra: Você pode ver quanto tempo falta para a próxima execução automática do seu cenário acessando o Dashboard no Make.
Salvar (Save)
Salva todas as alterações feitas no cenário.

Entradas do cenário (Scenario inputs)
As entradas de cenário são campos que você pode definir para enviar informações personalizadas ao iniciar um cenário. Eles funcionam como "variáveis de entrada", ou seja, o cenário só começa com base nas informações que você fornece.

Você pode usar esses inputs de 3 formas diferentes:

Preencher manualmente ao rodar o cenário.
Enviar os inputs a partir de outro cenário.
Enviar os inputs pela API do Make.
Esse é um conteúdo um pouco mais avançado no Make, então sugiro uma lida em sua documentação para mais informações.
Configurações de cenário (Scenario settings)
No botão de configurações é possível ajustar as configurações avançadas do cenário. Essas configurações controlam como o cenário se comporta em situações de erro, como lida com dados sensíveis e até quantas vezes ele pode tentar rodar.

Esse é um conteúdo também está um pouco mais avançado, então, do mesmo modo, sugiro ler a documentação para mais informações.
Notas/Anotações (Notes)
É possível adicionar notas em cada módulo. Essas notas servem de documentação, registros ou avisos.

O botão permite você ver todas as notas adicionadas no cenário. Para adicionar uma nota a um módulo você pode clicar com o botão direito no módulo e selecionar a opção ”Add a note” (Adicionar uma nota).

Versões anteriores (Previous versions)
Essa opção permite que você possa acessar antigas versões do projeto que foram salvas, mas já modificadas.

Auto-alinhamento (Auto-align)
Essa opção permite a visão centralizada e alinhada de todo o processo construído.

Mais opções (More)
Esse botão mostra três novas opções para o cenário.

Alt text: A imagem mostra o menu expandido do botão de três pontos na barra de ferramentas da plataforma Make. As opções exibidas são “Explain flow” para explicar o fluxo, “Export blueprint” para exportar o plano do cenário e “Import blueprint” para importar um plano. Os ícones à esquerda de cada opção representam ações relacionadas à documentação e gerenciamento de fluxos automatizados.

Explicar o fluxo (Explain flow)
Essa opção mostra o caminho percorrido pela informação dentro do fluxo e como ela é passada por cada módulo.

Exportar blueprint (Export blueprint)
Permite você salvar em sua máquina o projeto que você construiu no make. O projeto é salvo em um arquivo JSON e pode ser compartilhado!

Importar blueprint (Import blueprint)
A importação do blueprint significa que você pode criar um cenário com base em um arquivo JSON que você tenha em sua máquina, criando a mesma estrutura de cenário descrita no arquivo JSON enviado.

Módulos
O Make disponibiliza seus módulos de fácil acesso para quem está desenvolvendo o projeto. Esses módulos são os chamados, módulos “build-in” do Make, pois são do próprio Make. Entre eles estão o controle de fluxo, ferramentas e text parse, os quais, durante o projeto do curso, trabalhamos com todos eles.

Adição (Add)
Nesse botão podemos buscar, selecionar e adicionar um novo módulo ao cenário.

@@10
Para saber mais: Como enviar e-mails com Make+Outlook

Durante nosso projeto buscamos automatizar a criação de e-mails de resposta para clientes que perguntem algo que possa ser respondido pelo FAQ. O e-mail criado é apenas um rascunho que pode ser revisado antes de ser enviado como resposta.
No entanto, existe a opção de enviar diretamente o e-mail para o destinatário no Make. Ela pode ser acessada no módulo Microsoft 365 Email (Outlook) e a função ”Creat and Send a Message” (Criar e Enviar uma Mensagem).

Alt text: A imagem mostra a interface do Microsoft 365 Email (Outlook) na plataforma Make, com o módulo “Create and Send a Message” destacado.

Nela, basta usar da sua atual conexão da Microsoft e preencher os campos de informações de envio. Os campos são os mesmo que vimos durante os vídeos, portanto, você pode preencher do mesmo modo.

Alt text: A imagem mostra o formulário de configuração do módulo “Create and Send a Message” na plataforma Make para envio de e-mails. Os campos obrigatórios incluem “Subject”, “Body Content” e “To Recipients”. Também estão disponíveis os campos opcionais “Importance”, “To Recipients”, “From” e “Reply To”, além da opção “Show advanced settings” desativada. No rodapé da tela, há os botões “Cancel” e “Save”.

Super simples, não é?

@@11
Projeto final

Você pode baixar o projeto deste curso nesse link. Esse arquivo é conhecido por blueprint, ele tem o formato JSON e consegue salvar todas as estruturas criadas em um projeto, permitindo que ele possa ser salvo na máquina e compartilhado.
Para você importar esse projeto no seu cenário basta criar um novo cenário, acessar na barra localizada na parte inferior um botão com “...” (More) e, em seguida, clicar na opção “Import blueprint”.

Alt text: A imagem mostra a barra de um cenário na plataforma Make, com o menu de opções extras expandido. Uma seta vermelha aponta para a opção “Import blueprint”.

Envie o arquivo que você baixou e prontinho! O projeto está em seu cenário!

Lembre-se de adicionar suas conexões em cada módulo para salvar seu projeto no Make.

https://cdn3.gnarususercontent.com.br/4454-make/Projetos/projeto-blueprint.json

@@12
Conclusão

Parabéns por ter concluído este curso. Ficamos genuinamente muito felizes por ter acompanhado vocês até aqui. Embora tenha sido uma caminhada mais curta, vimos que o MAKE é muito simples de usar, e o suporte que a ferramenta nos oferece é bastante intuitivo.

Quais são as recomendações que trazemos? Além dos vídeos já publicados, sugerimos que vocês explorem as atividades deste curso e busquem se aprofundar na ferramenta, utilizando outros módulos. Não se limitem apenas aos vídeos.

Incentivando a criação de automações e suporte comunitário
Além disso, incentivamos a criação de novas automações, algo que esteja mais alinhado com a realidade de cada um. Caso surjam dúvidas, por favor, consultem nosso fórum. Também temos o Discord e, de forma altruísta, incentivamos que ajudem outros estudantes que tenham dúvidas relacionadas, as quais vocês possam responder.

Estruturando o fluxo no MAKE
Durante a aula, nós construímos todo o nosso fluxo dentro do MAKE, desde a coleta do dado, do e-mail recebido, até o final, decidindo se iríamos apenas organizar o nosso fluxo ou realmente responder ao e-mail. Construímos todo esse fluxo, que está bem estruturado. Se explicarmos o fluxo, ele se apresenta de forma clara e organizada.

Personalizando e compartilhando o projeto
Conseguimos adicionar módulos e várias funções do MAKE para transformar uma tarefa repetitiva e demorada em algo simples, direto e operacional, tornando o processo mais rápido e efetivo. Para personalizar ainda mais o projeto, podemos clicar com o botão direito em qualquer módulo e selecionar a opção Rename, para dar um nome ao módulo relacionado à sua função, tornando o projeto mais personalizado.

Além disso, como criamos este projeto, podemos compartilhá-lo em nosso portfólio e também no LinkedIn. Marque a Alura e nós no LinkedIn, mostre o trabalho que está realizando e traga visibilidade ao seu nome.

Solicitando feedback e despedida
Por favor, não se esqueça de avaliar este curso, deixando nos comentários sugestões de melhorias ou sua opinião sobre o que achou. Nos vemos na próxima aula. Até mais!

@02-Praticando automações no Make

@@01
Mão na massa: Automatização de alertas de estoque
 PRÓXIMA ATIVIDADE

Vamos buscar praticar nossos novos aprendizados entrando em outros contextos para resolver novos problemas!
Atividade
Você é responsável pela gestão de uma loja online com diversos tipos de produtos, e precisa garantir que o estoque esteja sempre disponível para atender aos pedidos. A loja possui uma regra clara: sempre que a quantidade de um item estiver igual ou abaixo de 3 unidades, é necessário repor o estoque. Para evitar controle manual e perda de tempo, você decide automatizar esse processo usando o Make. A ideia é identificar os produtos com estoque baixo e gerar automaticamente um e-mail para a pessoa responsável por aquele tipo de item solicitando a reposição.

Você tem dois conjuntos de dados: um com os produtos e suas quantidades em estoque, e outro com o e-mail do responsável por cada produto. Esses dados podem ser organizados em duas tabelas no Excel e acessados via Make.

Dados 1: Estoque

Produto	Quantidade em Estoque
Fone Bluetooth Pro	12
Carregador USB-C 20W	3
Teclado Mecânico RGB	7
Camiseta Básica Preta	25
Jaqueta Corta Vento	2
Calça Jeans Slim	6
Tênis Esportivo Branco	4
Sandália Feminina Couro	10
Bota Masculina Marrom	1
Mochila Executiva Nylon	9
Relógio Digital Casual	15
Óculos de Sol Unissex	5
Livro: “A Arte da Guerra”	18
Caderno Capa Dura 200p	8
Caneta Esferográfica Kit	2
Dados 2: Responsáveis

Produto	Responsável (E-mail)
Fone Bluetooth Pro	eletronicos@email.com
Carregador USB-C 20W	eletronicos@email.com
Teclado Mecânico RGB	eletronicos@email.com
Camiseta Básica Preta	roupas@email.com
Jaqueta Corta Vento	roupas@email.com
Calça Jeans Slim	roupas@email.com
Tênis Esportivo Branco	calcados@email.com
Sandália Feminina Couro	calcados@email.com
Bota Masculina Marrom	calcados@email.com
Mochila Executiva Nylon	acessorios@email.com
Relógio Digital Casual	acessorios@email.com
Óculos de Sol Unissex	acessorios@email.com
Livro: “A Arte da Guerra”	papelaria@email.com
Caderno Capa Dura 200p	papelaria@email.com
Caneta Esferográfica Kit	papelaria@email.com
Acesse o arquivo com as tabelas dessa atividade e da próxima nesse link
Portanto, crie uma automação no Make que:

Leia os dados do estoque e identifique quais produtos estão com quantidade igual ou menor que 3;
Localize o e-mail do responsável por cada um desses produtos com base na segunda planilha;
Envie um e-mail automático solicitando a reposição do item, informando o nome do produto e a quantidade atual em estoque.
Dica: Você pode apenas gerar um rascunho de e-mail com Groq ao invés de enviar um e-mail de fato.

Existem várias formas de resolver esse problema e eu irei apresentar uma delas! Mas você sempre pode usar sua criatividade para construir da sua forma e ver o projeto funcionar!
A ideia de fluxo para o projeto será: Leitura dos dados de estoque > filtragem apenas dos produtos com baixa quantidade > leitura dos dados de contato > envio dos dados de estoque e contato para a IA gerar um e-mail > geração de e-mail.

Começamos adicionando o módulo do Excel para coletar a planilha de estoque. Então adicionamos o módulo Microsoft 365 Excel e a função List Worksheet Rows. Na configuração, iremos adicionar nossa planilha de Estoque de produtos.

Alt text: A imagem mostra a configuração de um módulo do Microsoft 365 Excel na plataforma Make. Os campos preenchidos indicam a seleção do método, o local do OneDrive definido como “My Drive”, o arquivo chamado “Planilha de mão na massa.xlsx” e a planilha “Estoque de produtos”. A opção “Skip All Rows After a Blank Row” está marcada como “Yes”, e o campo “Limit” para número máximo de resultados está vazio. Há botões “Cancel” e “Save” no rodapé da janela.

De modo similar, seguimos para a coleta de contatos dos responsáveis pelo estoque. Utilizamos o mesmo módulo e função (Microsoft 365 Excel e List Worksheet Rows) para acessar os contatos. A diferença está apenas na planilha utilizada, pois agora será a planilha de contatos.

Antes de seguir para o próximo passo, iremos colocar um filtro na linha que liga as duas consultas de planilha. Basta apenas clicar na linha que liga os módulos e definir o filtro.

Alt text: A imagem mostra dois módulos conectados na plataforma Make, ambos do Microsoft Excel. À esquerda está o módulo “Planilha estoque” e à direita o “Planilha contatos”, ambos configurados para listar linhas de planilhas. Entre os dois módulos há uma seta vermelha apontando para o ponto de conexão central, indicando a rota entre eles.

Dei o nome do filtro de “Filtro de baixo estoque” e a condição é que o valor da quantidade de estoque deve ter um valor menor ou igual a 3 como especificado na imagem.

Alt text: A imagem mostra a configuração de um filtro na plataforma Make, com o título “Filtro de baixo estoque”. A condição definida avalia se o valor da coluna “Quantidade em Estoque” é menor ou igual a 3. Há botões para adicionar regras adicionais com operadores AND ou OR, além das opções “Cancel” e “Save” no rodapé da janela.

Com esse filtro, limitamos que apenas os pedidos que precisam de estoque entrem no fluxo e façam a execução desejada na automação.

Agora partimos para a continuidade do fluxo. Vamos voltar para coleta de contatos dos responsáveis. Para facilitar o encontro do contato correto pela IA, é necessário que ele possa ver todo o texto da tabela, logo iremos utilizar uma ferramenta de agregação de texto. Para isso acessamos o módulo de Tools e a função Text aggregator.

A agregação de texto vai gerar uma tabela que lista o nome do produto seguido com o contato do responsável.

Alt text: A imagem mostra a configuração de uma ferramenta na plataforma Make para agregar dados da planilha “Planilha contatos” do Excel. O módulo de origem selecionado é o que lista as linhas da planilha, o separador de linhas está definido como “New row” e não há agrupamento configurado. Na área de texto, foram selecionados os campos “Produto” e “Responsável (E-mail)” do excel e colocados entre barras verticais. A opção “Show advanced settings” está ativada e os botões “Cancel” e “Save” aparecem no canto inferior.

Agora com todos os dados coletados, podemos seguir para a geração de uma mensagem com a IA. Utilizaremos o módulo do Groq para utilizar os modelos disponíveis. Para isso, adicionamos o módulo de Groq e a função Create a JSON Chat Completion.

O modelo utilizado é o llama-3.3-70b-versatile e nosso prompt do sistema é:

O JSON deverá conter informações suficientes para enviar o e-mail de notificação conforme o estruturado: 
 
{ 
  "e-mail responsavel": "e-mail", 
  "Assunto": "Notificação de baixa no estoque!", 
  "Texto-mensagem": "Mensagem criada" 
} 
 
O "Assunto" não deve ser alterado. Os valores das outras estruturas devem ser ajustados conforme a solicitação. 
COPIAR CÓDIGO
Já o prompt de usuário é:

Você é responsável por notificar setores responsáveis pelo estoque de itens para uma loja. A regra de estoque da loja é: quando temos valores de itens abaixo ou igual a 3, é necessário fazer a reposição. Para a reposição é necessário enviar um e-mail para o setor responsável, sua missão é criar esse e-mail. 
 
Abaixo informações sobre os produtos que estão com baixa quantidade: 
 
Produto: {{VARIÁVEL DO EXCEL - LINHA PRODUTO}} 
Quantidade em estoque: {{VARIÁVEL DO EXCEL - LINHA QUANTIDADE DO ESTOQUE}} 
 
Abaixo, a lista de contatos a depender do produto em falta: 
 
{{VARIÁVEL DO TOOLS- SAÍDA DE TEXTO}} 
 
Descubra qual o e-mail adequado para o contato. 
 
Crie um e-mail que notifica o setor responsável da situação atual e solicite a reposição dos itens o quanto antes. O e-mail deve ser profissional, objetivo e educado, não faça apresentação ou despedida. Use HTML para manter a estrutura adequada do e-mail. A composição do e-mail deve seguir a estrutura: 
 
[Texto de notificação da baixa quantidade do produto] 
[Texto de informações sobre o produto] 
 
[Texto de solicitação de reposição do estoque] 
COPIAR CÓDIGO
Com o texto de e-mail pronto, podemos seguir para a criação de uma mensagem que pode ser enviada. Para isso utilizaremos o Microsoft 365 Email (Outlook) e a função Create a Draft Message, pois estaremos criando uma mensagem de rascunho.

O assunto, mensagem e contato são especificados pela saída do Groq. Um detalhe é que eu escolhi adicionar uma alta importância ao rascunho visto que o estoque estaria baixo.

Alt text: A imagem mostra a configuração de criação de e-mail pelo módulo Microsoft 365 Email (Outlook) na plataforma Make. Os campos “Subject” e “Body Content” estão preenchidos com variáveis referentes ao assunto e conteúdo da mensagem gerados pelo Groq. A importância do e-mail está definida como “High” e o campo “To Recipients” contém um endereço dinâmico representado pela variável “e-mail responsável” do Groq. A opção de configurações avançadas está desativada, e os botões “Cancel” e “Save” aparecem na parte inferior.

Observamos que nosso projeto tem o seguinte fluxo:

Alt text: A imagem mostra um fluxo automatizado na plataforma Make com cinco módulos conectados. O primeiro módulo “Planilha estoque” lê linhas de uma planilha do Excel, seguido por um filtro nomeado “Filtro de baixo estoque”. O segundo módulo “Planilha contatos” também lê dados de uma planilha. Em seguida, o módulo “Tools” agrega texto com base nas informações recebidas. O quarto módulo “Criando o e-mail” utiliza um modelo de linguagem para gerar o conteúdo do e-mail, e o último módulo “Microsoft 365 Email (Outlook)” cria uma mensagem de e-mail como rascunho.

Com isso, podemos executar nosso projeto e ver os resultados. Ao clicar em “Run once” (Executar uma vez), esperar o fim do resultado e verificar no Outlook a pasta de rascunho.

Alt text: A imagem mostra a caixa de rascunhos de e-mails, com quatro mensagens destinadas a diferentes endereços de contato: papelaria, calçados, roupas e eletrônicos. Todas têm o título “Notificação de baixa no e...” e exibem um alerta de prioridade com ponto de exclamação vermelho. As mensagens informam sobre a baixa no estoque de produtos como “Caneta Esf...”, “Carrega...” e outros, com os conteúdos parcialmente visíveis.

Com isso, conseguimos criar uma solução para o problema!

Baixe aqui o blueprint do projeto, caso queira conferir como fiz.

@@02
Mão na massa: Categorizando e-mails
 PRÓXIMA ATIVIDADE

Atividade
Você é líder de um time de vendas, por isso recebe constantemente muitos e-mails com diversos propósitos dentro do contexto do trabalho. Para evitar um acúmulo de e-mails em sua caixa de mensagem e buscando organizar o que você recebe, você decide usar o Make para automatizar a categorização dos e-mails do trabalho.

Existem quatro categorias que te interessam categorizar no momento: Reuniões e Agendamentos, Solicitação de Aprovações, Problemas e Urgências e Não categorizado.

Para a implementação adequada da organização você vai precisar criar essas pastas no seu Outlook.
Na tabela abaixo está a definição de cada categoria. Você pode copiá-la e colar em uma planilha do Excel para acessá-la pelo Make.

Categoria	Descrição
Reuniões e Agendamentos	E-mails relacionados a convites, confirmações, reagendamentos ou cancelamentos de reuniões e eventos internos. Palavras-chave: "agendar reunião", "remarcar", "confirmação de reunião", "link da chamada".
Solicitação de Aprovações	Pedidos que exigem autorização, como aprovações de compras, novos projetos, contratações ou qualquer decisão que precise do aval da gestão. Palavras-chave: "aprovação necessária", "pedido de autorização", "precisamos da sua aprovação".
Problemas e Urgências	E-mails que relatam falhas, incidentes operacionais, crises ou qualquer situação que exige resposta imediata. Palavras-chave: "urgente", "problema crítico", "precisamos resolver rápido", "incidente", "paralisação".
Não categorizado	E-mails que não se encaixam em nenhuma das categorias acima.
Faça um cenário no Make que permita que os e-mails recebidos por você possam ser automaticamente categorizados de acordo com a tabela acima, com base no conteúdo do e-mail, e movidos para a pasta correspondente no seu Outlook.

Dica: Para montar isso, é necessário que você crie pastas no seu outlook com o nome dessas categorias.

Existem várias formas de resolver esse problema e eu irei apresentar uma delas! Mas você sempre pode usar sua criatividade para construir da sua forma e ver o projeto funcionar!
A ideia de fluxo para o projeto será: Leitura dos e-mails > leitura das categorias e descrições > definição da categoria > realocação do e-mail.

Começamos adicionando o módulo do Outlook para ler os e-mails. Adicionamos ele com o módulo Microsoft 365 Email (Outlook) e a função Search Messages. Iremos definir a caixa de entrada como a pasta principal e o limite de mensagens, vamos definir como 1 (valor bem opcional).

Com isso, seguimos para a adição do módulo do Excel para coletar a descrição das categorias. Então adicionamos o módulo Microsoft 365 Excel e a função List Worksheet Rows. Na configuração, iremos adicionar nossa planilha de Estoque de produtos.

Para que todo o texto da planilha fique disponível para a IA conseguir definir a categoria, iremos utilizar da ferramenta de agregação de texto do Make. Então iremos adicionar no fluxo o módulo de Tools e a função Text aggregator. O módulo que iremos utilizar para agregar será o Excel, e iremos alocar o texto de Categoria e Descrição separados por barras verticais (|).

Agora podemos adicionar o módulo do Groq para solicitar que a IA consiga identificar a categoria adequada para o e-mail. Adicionamos então o módulo do Groq com a função Create a JSON Chat Completion.

O modelo utilizado é o llama-3.3-70b-versatile e nosso prompt do sistema é:

De acordo com a solicitação, você deve retornar o seguinte JSON como resultado. 
 
{ 
  "categoria" : "categoria encontrada" 
} 
COPIAR CÓDIGO
Já o prompt de usuário é:

Você é um assistente especializado em categorização de e-mails para gestão. Sua tarefa é ler o conteúdo do e-mail e classificá-lo em uma das seguintes categorias pré-definidas. Retorne apenas o nome da categoria mais adequada. Se o e-mail não se encaixar em nenhuma categoria, retorne "Não categorizado". 
 
Abaixo estão as categorias e suas descrições: 
 
{{VALOR DE TOOLS - TEXTO}} 
 
Agora, classifique o seguinte e-mail: 
Assunto: {{VALOR DO OUTLOOK - SUBJECT (ASSUNTO)}} 
Conteúdo:  
{{VALOR DO OUTLOOK - BODY > CONTENT (CONTEÚDO)}} 
 
Retorne apenas a categoria correspondente. 
COPIAR CÓDIGO
Ao fim, vamos executar todo o projeto, clicando no botão “Run once” para obtermos uma variável de saída do módulo do Groq.

Com isso conseguimos obter o resultado da categoria do e-mail. Esse resultado vai definir para onde esse e-mail será movido. Utilizaremos o módulo de rotas junto a filtros para definir qual automação será feita. Nosso objetivo com isso é que, dependendo da categoria retornada, o fluxo de processo siga apenas um dos caminhos especificados.

Portanto, adicionamos ao fluxo o módulo de rota, para adicioná-lo é bem simples, basta buscar pelo módulo de Flow Control e selecionar a função Router. Adicionamos caminhos clicando com botão esquerdo em cima do módulo de rotas. No primeiro caminho adicionamos o módulo Microsoft 365 Email (Outlook) e a função Move a Message. No módulo iremos definir o ID da mensagem que será movida como o ID da mensagem que foi lida e o novo folder que será movido como o folder de “Reuniões e Agendamentos”.

Para que essa movimentação seja bem eficaz, precisamos definir o filtro que vai permitir que apenas a classificação de e-mail “Reuniões e Agendamentos” passe por essa rota. Para construir isso, adicionamos um filtro na linha de rota clicando em cima da linha que conecta os dois módulos.

A configuração do filtro deverá ser que o valor resultante da saída do Groq seja igual a Reuniões e Agendamentos.

Com isso definimos nossa primeira rota.

O processo para as demais é bem similar, de modo que a única diferença é o valor da condição do filtro e para onde vai o e-mail (Solicitação de Aprovações, Problemas e Urgências ou Não categorizado). Então repetimos o mesmo processo para as demais categorias e ao fim temos o fluxo final.

Ao executar a automação o e-mail que está na caixa de mensagens será movido para alguma das pastas criadas a depender do conteúdo dentro dela.

Com isso, conseguimos criar uma solução para o problema!

Baixe aqui o blueprint do arquivo.

https://cdn3.gnarususercontent.com.br/4454-make/Projetos/mao-na-massa-01.json