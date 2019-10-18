# cnpq-paper-co-financing

## Descrição

Relatório sobre o cofinanciamento de artigos cinetíficos no Brasil

## Description

Report about co-financing of scientific papers in Brazil

## **Introdução**

Considerando o documento da Estratégia Nacional de Ciência, Tecnologia e Inovação (ENCTI), o desenvolvimento da ciência e da tecnologia está diretamente ligado ao método estratégico que cada país adota, sendo os governos nacionais um dos principais protagonistas para elaborar e por em práticas políticas e investimentos que impulsionam e ampliam o avanço do desenvolvimento da pesquisa e da inovação, pois, se, somado a isso, levarmos em conta a conclusão do relatório Estadunidense de pesquisa, inovação e ciência de 2012, o “Research, Development, Innovation and the Science and Engeneering Workforce”, o investimento público é essencial para o desenvolvimento cientifico e tecnológico de forma mais ampla e completa, já que, o investimento público tende a atender áreas que o investimento privado não atende com tanto volume, especialmente quando se trata de ciências de base ou pesquisas sem perspectivas diretas ou imediatas de aplicação, ressaltando ainda mais o papel importantíssimo do Governo em relação ao fomento à pesquisas. Diversos agentes públicos participam do processo de desenvolvimento científico e tecnológico e, entre eles, estão as agências de fomento, que são responsáveis por apoiar financeiramente as iniciativas de pesquisas e assim atender diversas demandas dos pesquisadores. Tratando-se novamente das informações presentes no ENCTI, no Brasil, várias agências de fomento participam desse processo, algumas possuindo ligação direta ou indireta com o governo federal, enquanto outras são ligadas aos governos estaduais, além disso, essas agências são as principais e mais participativas fontes de investimento para elaboração de pesquisas no Brasil. 

Segundo um estudo elaborado pela USP, “Quem financia a pesquisa brasileira? Um estudo InCites sobre o Brasil e a USP”, as três principais agências de fomento brasileiras por número de artigos financiados são, respectivamente do maior resultado para a menor, o CNPq, a CAPES e a FAPESP, justamente as três agências que serão analisadas nessa pesquisa. Esse estudo da USP chegou a esse resultado utilizando as ferramentas disponíveis no Web of Science, um ambiente online para busca de documentos científicos indexados e para análises de dados relacionadas a esses documentos, que utiliza uma base de dados, mantida pela Clarivate Analytics, bem vasta e diversificada, contendo uma série de artigos e outros tipos de documentação científica produzidos e indexados ao redor do mundo. Nesse contexto, um documento indexado é aquele que está presente em alguma base de dados que forneça algum tipo de interação que permita que esse documento seja encontrado, podendo o acesso a esse documento ser público ou não, além disso, como a indexação é um processo criterioso e que necessita de diversas etapas e processos seletivos para um pesquisador ter o próprio trabalho indexado, essas bases de dados possuem um alto nível de credibilidade. O Web of Science fornece artifícios para realizar pesquisas mais avançadas que gerem informações adicionais além da visualização do artigo indexado em si, tais como agências financiadoras, universidades, autores, países, datas, áreas do conhecimento etc. E, é a partir daí que os dados, não apenas da pesquisa da USP citada, mas também dessa pesquisa foram coletados (mais informações estarão disponíveis no próximo tópico que tratará sobre a metodologia).

O tipo de cofinanciamento que será retratado nesse documento será relacionado especificamente ao cofinanciamento voltado para o fomento à produção de artigos científicos. Essa pesquisa considera artigos científicos que foram financiados por mais de uma agência de fomento, ou seja, duas ou mais agências que, juntas, forneceram verba para o mesmo pesquisador, ou para o mesmo grupo de pesquisadores, que produziu o mesmo artigo somando os auxílios dessas mesmas agências. Existem diversos estudos e portais de transparência que é possível observar, alisar e tirar conclusões sobre as ações de fomento dessas agências, porém, não existem muitas formas de analisar como essas agências trabalham juntas, especialmente no âmbito de cofinanciamento de artigos. Portanto, o objetivo desse documento será justamente preencher essas lacunas e trazer uma visão mais clara sobre o cofinanciamento de artigos. Portanto, nesse documento, serão apresentados alguns gráficos correlacionando dados extraídos do Web of Science referentes às três principais agências de fomento por número artigos financiados (CNPq, CAPES e FAPESP) e, somado a isso, também serão traçadas observações e discussões entorno dos gráficos, sendo possível assim, elaborar visões mais claras e interessantes que podem ser úteis para nortear o futuro das ações públicas, tanto do governo como um todo, quanto internamente nas próprias agências, além disso, esses dados e discussões também servirão como mais uma fonte para a sociedade conseguir observar de forma mais clara, objetiva e transparente as ações e os resultados dessas agências.

## **Metologia**

Os dados extraídos para construção dos resultados dessa análise foram coletados a partir da plataforma Web of Science. Essa plataforma possui um ambiente de pesquisas avançadas, que foi utilizado para realizar filtragens específicas que mostrem uma base de dados sobre o acumulado de artigos científicos financiados pelas três maiores agências de fomento nacionais já citadas (CNPq, CAPES e FAPESP) entre 2012 e 2019. A partir dos dados coletados diretamente do Web of Science, arquivos em CSV (Comma-separated values), foram montados gráficos utilizando a linguagem de programação Python junto a biblioteca Matplotlib.

### **Estratégia de Filtragem**

As pesquisas avançadas do Web of Science trabalham com rótulos e  operadores boolianos. O rótulo para a filtragem por agência financiadora é “FO = ()”. Dentro dos parênteses deve ser colocado todos os possíveis nomes das agências, que são separados por “*” seguido do operador booleano “OR”. 
Para cada agencia foi usado os seguintes códigos de pesquisa:

> CNPq: FO=(CNPq* OR Conselho Nacional de Desenvolvimento Científico e Tecnológico* OR Conselho Nacional de Desenvolvimento Científico e Tecnológico CNPq* OR National Council for Scientific and Technological Development* OR National Council for Scientific and Technological Development CNPq* OR Conselho Nacional de Pesquisa* OR Brazilian National Council for Scientific and Technological Development*)

> CAPES: FO = (CAPES* OR Coordenação de aperfeiçoamento de pessoal de nível superior* OR Coordenação de aperfeiçoamento de pessoal de nível superior CAPES* OR CAPES Brazil* OR CAPES Brasil* OR Coordenação de aperfeiçoamento de pessoal de nível superior Brasil* OR Coordination of Superior Level Staff Improvement CAPES* OR Coordination of Superior Level Staff Improvement* OR Coordination of Superior Level Staff Improvement Brazil*)

> FAPESP: FO = (FAPESP* OR FAPESP Brasil* OR FAPESP Brazil* OR Fundação de Amparo à Pesquisa do Estado de São Paulo* OR Fundação de Amparo à Pesquisa do Estado de São Paulo FAPEPSP* OR São Paulo Research Foundation FAPESP* OR São Paulo Research Foundation)

Para filtrar especificamente os artigos financiados por mais de uma das agências citadas, foi utilizado o operador booleano “AND”.

## **Data de Extração e do Universo dos Dados**

Como o Web of Science passa por atualizações de dados simultâneas ao cadastro de novos artigos, todos os gráficos e resultados estão desatualizados e restritos ao universo da data de extração (dia 27 e 28 de Fevereiro de 2019). Além disso, foram considerados apenas os artigos publicados de Janeiro 2012 até o dia 28 de Fevereiro de 2019.

## **Observações Sobre o Web of Science**

O Web of Science não é uma base de dados perfeita e, portanto, possui algumas limitações nos filtros que acabam ocasionando em uma margem de erro em todos os gráficos. Uma das limitações é a impossibilidade de filtrar artigos que foram financiados por apenas uma agência financiadora, já que, o Web of Science, não separa esses artigos dos artigos com mais de uma agência e, portando, os resultados não só mostram os artigos financiados por apenas uma agência especifica, mas também, mostram os artigos financiados por essa agência junto com várias outras, não especificando de forma clara e separada a quantidade de artigos financiados por essa única agência sozinha. Além disso, o Web of Science também possui um problema com duplas contagens e sobreposição de dados, fazendo com que, na mesma base dados, o mesmo artigo apareça mais de uma vez e, com isso, acaba sendo adicionado ao resultado final, sendo assim, impossível filtrar esses artigos repetidos. Outra limitação é o universo da plataforma, mesmo o Web of Science sendo uma base de dados muito boa e completa, o site claramente não apresenta o total verdadeiro de artigos publicados, sendo limitado ao que ele possui nas próprias bases de dados.

# **RESULTADOS**

## Comparativo Entre as Agências

![grafico1](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/comparativo.png)

O gráfico acima traça um comparativo do acumulado da produção anual de artigos fomentados pelas três principais agências de fomento nacionais. Observa-se que o CNPq é a agência que mais fomenta artigos no Brasil.
Levando em consideração esses dados, os gráficos abaixo trarão uma visão mais clara sobre as relações entre as agências de fomento, considerando o cofinanciamento como parte principal da análise.

![grafico2](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/capesxcnpq.png)

![grafico3](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/fapespxcnpq.png)

O gráfico da direita responde a pergunta, “Dos artigos financiados pela CAPES, quantos possuem cofinanciamento com o CNPq?”. A barra laranja e a barra azul são, no todo, uma única barra que representa o acumulado anual de artigos fomentados pela CAPES, a parte azul representa quantos desses artigos foram fomentados pela CAPES junto com o CNPq, mostrando um valor percentual na frente da barra que representa a porcentagem referente à quantidade de artigos cofinanciados por essas duas agencias juntas em relação ao todo. O gráfico da esquerda representa a mesma análise, porém fazendo um comparativo da participação do CNPq em relação a FAPESP.

## **Análise de Cofinanciamento (Participação da CAPES)**

![grafico4](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/cnpqx.png)

![grafico5](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/fapespxcapes.png)

## **Análise de Cofinanciamento (Participação da FAPESP)**

![grafico6](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/cnpqxfapesp.png)

![grafico7](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/capesxfapesp.png)

## **Diagrama de Venn Sobre o Cofinanciamento**

![grafico8](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/venn.jpg)

Os valores dentro do diagrama representam o acumulado de artigos fomentados por essas agências entre 2012 e Fevereiro de 2019. As áreas de interseção representam a quantidade de artigos que possuem cofinanciamento entre as respectivas agências. As áreas sem intersecção não só representam apenas os artigos sem cofinanciamento, mas também artigos cofinanciados com outras agências que não foram consideradas na análise.

## **Interseções do Diagrama (Análise das Principais Universidades em Números de Artigos Cofinanciados)**

### CAPES ∩ CNPq (10 principais universidades)

![grafico9](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/universidadescapesxcnpq.jpg)

O gráfico acima mostra as 10 principais universidades que produziram artigos com o cofinanciamento entre CAPES e o CNPq.

### FAPESP ∩ CNPq (5 principais universidades)

![grafico10](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/universidadesfapespxcnpq.jpg)

### FAPESP ∩ CAPES (5 principais universidades)

![grafico11](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/universidadesfapespxcapes.jpg)

### FAPESP ∩ CNPq ∩  CAPES (5 principais universidades)

![grafico12](https://github.com/LucasGuerraCavalcante/cnpq-paper-co-financing/blob/master/img/universidadesostres.jpg)

## **O Resto do Relatório Ainda Está em Construção**
## **The report still on progress**

### Referências

> http://www.finep.gov.br/images/a-finep/Politica/16_03_2018_Estrategia_Nacional_de_Ciencia_Tecnologia_e_Inovacao_2016_2022.pdf

> https://nsf.gov/nsb/publications/2012/nsb1203.pdf

> http://www.sibi.usp.br/noticias/quem-financia-a-pesquisa-brasileira-um-estudo-incites-sobre-o-brasil-e-a-usp/

> http://wokinfo.com/

> https://www.ufrgs.br/bibeng/wp-content/uploads/2016/04/Indexa%C3%A7%C3%A3o-de-Peri%C3%B3dicos.pdf



