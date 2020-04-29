---
title: "Aplicação de Redes Neurais Profunda em Reconhecimento Facial"
authors:
- mesquita
date: "2019-07-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *Source Themes Conference*
publication_short: In *STC*

abstract: This work has the purpose of demonstrating the application of the Deep Neural Network in Facial Recognition, presenting the functionalities of this network in image processing in a facial recognition software, also focusing on Machine Learning, with emphasis on detailing the routines of calculations involved in the formulas used in training and learning machines, existing databases for training and development of facial recognition applications, the use of OpenCV algorithms Eigenfaces, FisherFace and LBPH. All this to highlight the advantages in the use of software with facial recognition, the confidence and acceptability of this solution, be it in the area of ​​security, distance education - EAD and in other applications that require authentication by biometrics. According to the literature, most authors agree that facial recognition is the most promising area of ​​artificial intelligence, the fastest growing and its neural networks are constantly being used in information processing and machine learning

# Summary. An optional shortened abstract.
summary: Este trabalho tem a finalidade de demonstrar a aplicação da Rede Neural Profunda em Reconhecimento Facial, apresentando as funcionalidades desta rede no processamento de imagens em um software de reconhecimento facial, abordando ainda sobre aprendizado de máquina ou $Learning machine$, com ênfase no detalhamento nas rotinas dos cálculos envolvidos, nas fórmulas utilizadas no treinamento e aprendizado de padrões, bancos de dados existentes para treinamento e desenvolvimento das aplicações de reconhecimento facial, a utilização dos algoritmos da biblioteca OpenCV, do $Eigenfaces$, do $FisherFaces$ e do $LBPH$. Tudo isto para evidenciar as vantagens na utilização de software com reconhecimento facial, o grau de confiança e aceitabilidade deste tipo de solução, seja na área de segurança, da educação a Distância - EAD e em outras aplicações que requeira autenticação por biometria. De acordo com a literatura existente, grande parte dos autores concorda que o reconhecimento facial é a mais promissora área da Inteligência artificial, sendo a que mais cresce e suas redes neurais estão sendo utilizadas constantemente no processamento das informações e no aprendizado de máquinas.

tags:
- Source Themes
featured: true

links:
- name: Custom Link
  url: http://example.org
url_pdf: http://eprints.soton.ac.uk/352095/1/Cushen-IMV2013.pdf
url_code: '#'
url_dataset: '#'
url_poster: '#'
url_project: ''
url_slides: ''
url_source: '#'
url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---

{{% alert note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /alert %}}

{{% alert note %}}
Click the *Slides* button above to demo Academic's Markdown slides feature.
{{% /alert %}}

Supplementary notes can be added here, including [code and math](https://sourcethemes.com/academic/docs/writing-markdown-latex/).


# Introdução 

Nos dias atuais muito se fala sobre novas tecnologias, aprendizado de máquina,\gls{IOT}, automação, sistemas inteligentes e redes de processamento e mineração de dados de alta complexidade e \gls{IA}. É fato que estamos vivendo na era da 4º evolução industrial ou Industria 4.0, termo sugerido pelo alemão Klaus Schwab \cite{schwab2019quarta} que em seu livro \textit{ A Quarta Revolução Industrial}  afirma que “A quarta revolução industrial não é definida por um conjunto de tecnologias emergentes em si mesmas, mas a transição em direção a novos sistemas que foram construídos sobre a infraestrutura da revolução digital”, este conceito de integrar tecnologia a diversos setores, tais como comunicação, economia, medicina, automação, computação e telecomunicações, esta nova evolução tem a finalidade de facilitar a vida do ser humano, ofertando o conforto de realizar determinadas tarefas geralmente comuns, contínuas e repetitivas de forma automatizada, com resultados eficientes, logo as tecnologias que fazem parte da 4ª Evolução Industrial não estão restritas aos universos da nanotecnologia, neurotecnologia, biotecnologia, robótica, inteligência artificial e armazenamento de energia, sempre existirá algo mais a ser melhorado.

Quando falamos em novas tecnologias e evolução tecnológica, logo nos vem em mente a formosa \textit{Inteligência Artificial}, que para muitos causa espanto, sendo que no mundo acadêmico, é um ramo da ciência da computação que tem muito a oferecer e a ser estudado, seja na área da \gla{IA} Forte ou Fraca. Ou seja, é a arte de desenvolver algoritmos computacionais inteligentes, capazes de agir de forma intuitiva e com autossuficiência, não está tão distante, pois já existem algoritmos que simulam o raciocínio humano, sendo objeto constante de estudos e inovações.

Este trabalho começa relatando alguns fatos históricos que deram início a trajetória evolutiva da Inteligência Computacional ou Inteligência Artificial, com foco na evolução de suas diversas áreas, dando ênfase as técnicas das Redes Neurais Artificiais\gls{RNA}, ao aprendizado de máquinas $Machine Learning$, passando pelas técnicas de aprendizado de máquinas empregadas nas redes neurais profundas, o treinamento de reconhecimento de padrões, demostra  cálculos e fórmulas utilizados nass redes neurais e no aprendizado de máquinas e no próprio algoritmo de reconhecimento facial, a exemplo a \gls{DE} e o \gls{$k$NN} utilizadas nos algoritmos $Eigenface$, $FisherFace$, $LBPH$. Analisa o grau de confiança dos algoritmos testados, encerrado com a legislação vigente que regulamenta a utilização de sistemas de reconhecimento facial.

Partindo da publicação do artigo "Computing Machinery and Inteligence" \cite{turing1950computing}, o autor questiona se as máquinas poderiam realmente pensar? esta pergunta deu início as diversas discussões sobre a real possibilidade de um computador poder ou não pensar igual a um ser humano. Com vista a comprovar sua tese que as máquinas podem agir de forma similar ao comportamento humano, Allan Turing propôs um teste,  a fim de provar que as máquinas poderiam serem programadas e desenvolvidas para agir de forma análoga ao comportamento humano. Para isto, elaborou o famoso “Teste de Turring” ou jogo da imitação, que sugeria a interação entre o homem e máquina, partindo do princípio de que, as ações executadas por um computador programado para interagir com um usuário, respondendo perguntas de forma automática, poderia facilmente ser confundido como uma pessoa, sendo que em dado momento, tornaria impossível ao homem definir se as resposta viria realmente de uma pessoa ou de uma máquina programada para agir com tal.

Desde então, tivemos muitos avanços consideráveis no campo da IA, iniciando pela chamada era de ouro ou época do assombro que se deu em meados de 1956 até 1974, onde podemos pontuar vários fatos que marcaram esta época, por exemplo, a conferência de Darmouth \cite{mccarthy1955proposal} ocorrida em 1956, onde cientistas e especialista do campo da teoria da informação, se reuniram e trataram de diversos assuntos da evolução computacional, criaram então o geme da Inteligência Artificial ou simplesmente \gls{IA}, ano em que foi cunhado este termo, desde então esta área de estudo vem crescendo exponencialmente.

Nos dias atuais, no campo da Ciência da Computação, a \gls{IA} é área que mais se destaca, isto porque, a disciplina oferta diversas áreas do conhecimento a serem estudadas, tais como: as Redes Neurais Artificiais \gls{ANN}, O Aprendizagem de Máquinas - \textit{machine learning}, Visão Computacional, Analise e Síntese da voz e Lógica Difusa, são alguns exemplos.

Este trabalho envolve diversas áreas da IA, como as Redes Neurais Artificiais, Aprendizado de Máquina e Reconhecimento de padrões, fora o fato de que para elabora a fundamentação metodológica, envolve outras áreas do conhecimento, tais como, a Neurociência, Matemática, Filosofia e o Direito.

# Objetivos gerais e específicos

O objetivo deste trabalho é demonstrar as particularidades do funcionamento das Redes Reunais Profunda no processo de aprendizado em um software desenvolvido na linguagem de programação JAVA, especificamente para reconhecimento facial, sua base de programação, o uso das  Bibliotecas do \gls{OpenCV} e JAVACV, os métodos de reconhecimento e treinamento, o funcionamento dos algoritmos Eigenfaces, Fischerfaces e \gls{LBPH}, as diversas fórmulas matemática e cálculos envolvidos nos referidos algoritmos, o processamento as imagens, o uso dos bancos de testes e treinamentos, aplicabilidade e encerando com a legalidade de sistemas que usam dos sistemas de reconhecimento facial para detecção de pessoas.

# Metodologia

O método utilizado para a realização deste trabalho é o qualitativo, pois tem com a finalidade de analisar a aplicação das Redes Neurais Profunda em sistemas de reconhecimento facial, detalhando os cálculos empregadas na aplicação, bem como, detalhar os resultados obtidos e as normas e legislações vigentes no Brasil e no mundo que regulam o uso deste tipo de solução.

Para obter os dados necessários do estudo, foram feitas pesquisas bibliográficas de publicações nacionais e internacionais que tratam do assunto, bem como, em outros trabalhos acadêmicos e artigos científicos que abordam o tema. As obras e estudos analisados foram relacionados nas referências, onde constam todas literaturas consultadas e utilizadas diretamente para o desenvolvimento deste trabalho.

# Trabalhos Relacionados

Em pesquisas aos trabalhos relacionados sobre o tema, foram identificados várias publicações sobre os temas: Inteligencia Artificial, Redes Neurais, Learning Machine, Reconhecimento facial, os quais foram utilizados para fundamentar o objeto deste artigo.

partindo do principio da história das redes neurais, destacamos os patronos das redes neurais, Warren McCulloch e Walter Pitt,que em 1943 propuseram um modelo computacional de um neurônio artificial, com ligações de sinapses simulando o processamento da informação, utilizaram variáveis binárias, 0 ou 1, para simular o funcionamento do neurônio, os pesquisadores usaram a lógica Booleana e cálculos matemáticos para fundamentar das Redes Neurais Artificiais \cite{mcculloch1943logical}.

Em 1949,\cite{hebb1949organization} Donald Heeb neuropsicólogo canadense, introduziu em sua obra o primeiro método de treinamento para rede neural, suas opiniões sobre o aprendizado descrevem o comportamento e o pensamento em ternos de função cerebral, explicando os processos cognitivos das conexões entre neurônios.

Em 1950  Allan Turing, publica o Artigo "COMPUTING MACHINERY AND INTELLIGENCE" que inicia com a celebre frase “Eu proponho considerar a questão, as máquinas podem pensar?”, seu posicionamento despertou a curiosidade do mundo e deu início as diversas discussões sobre o polêmico assunto.  Turing queria que esta questão fosse respondida, para tanto afirmou na tese defendida que, se uma máquina pudesse interagir com um terço de seus interlocutores, interagindo e fazendo acreditar que seria um ser humano, então esta máquina pensaria como tal. Turing abriu precedentes para estudos relacionados a Inteligência das Máquinas, dando início então aos diversos campos de estudos da Inteligência Artificial. \cite{turing1950computing}

Em 1958 Frank Rosenblatt, implementou o primeiro modelo de Rede Neural multicamadas denominado o perceptron, formado de várias camadas de entrada e apenas uma camada de saída, sendo que para cada entrada existe um peso é relacionado, sendo que o valor de saída será a soma dos produtos de cada entrada pelo seu respectivo peso.\cite{rosenblatt1959perceptron}

Em 1961 Marvin Minsky publica o artigo "Passos em direção à Inteligência Artificial", reunindo os primeiros avanços no campo da IA, como trabalhos acadêmicos, experimentos, artigos, novas teses, servindo de inspiração a outros pesquisadores, impulsionando novas iniciativas de pesquisas na área.\cite{1998rnt}, sendo que em 1969, o autor publica outra obra com título semelhante Perceptron de Frank Rosenblatt, mostrando que o futuro desse modelo não era muito promissor, devido a grandes quantidade de cálculos envolvidos e aos poucos recursos computacionais existentes na época.\cite{minsky1988perceptrons}

Em 1986, Rumelhart, Hinton e Willams apresentaram um algoritmo que permitia ajustar os pesos em uma rede com mais de uma camada, denominado backpropagation, que foi criado a partir da generalização da regra de aprendizado “Widrow-Hoff”, conhecida como “regra Delta”, que fora introduzida por Bernard Widrow e Marcian Hoff entre 1960 e 1962 para redes do tipo feedfoward perceptron.

Entre 1987 a 1993, ficou conhecido como segundo inverno da \gls{IA}, publicações de artigo comprometendo e questionando as técnicas, as possibilidades e dificuldades de se implementar e trabalhar com grande volume de processamento de informações e cálculos, acompanhado de outras desilusões causaram uma verdadeira evasão de investimentos em pesquisas na área.

Em 1993 vivenciamos um novo despertar na área da \gls{IA} quando a IBM desenvolveu $Deep Blue$ ou azul profundo, um supercomputador criado especialmente para jogar xadrez, com capacidade de realizar cálculos otimizados e realizar cerca de 200 milhões jogadas por segundo, que derrotou o campeão mundial de xadrez Gary Kasparvov.

Estes acontecimentos trouxeram de volta o interesse em pesquisas e investimentos nas diversas áreas da \gls{IA}, outros acontecimentos reforçam ainda mais o interesse no campo de pesquisas, tipo o surgimento do carro autônomo desenvolvido pela Universidade de Stanford (EUA) em 2005; os assistentes virtuais, tais como a Alexia da Apple, a Cortana da Micrsoft e  Watson da IBM. A aprovação de um Software no teste de Turing, fato ocorrido em 2014. 

Todas estes fatos demostram o futuro potencial da \gls{IA} e seus diversos campos de pesquisa na evolução tecnologia, seja nas redes neurais, no aprendizado de máquina, no reconhecimento de padrões ou em outros conceitos que surgirão. É fato, o futuro é inevitável, só nos resta está preparados para viver estas mudanças.




