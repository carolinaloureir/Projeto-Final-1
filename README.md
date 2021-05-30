 <h1>Turismo em Portugal</h1>

![turismo-7](https://user-images.githubusercontent.com/84399844/119206661-aec46f00-ba93-11eb-924c-5f494137103e.png)

> 📅  Ultima atualização - 30 de Maio de 2021
## 🗒️ Contexto
No âmbito da unidade curricular Programação e Algoritmos II do 1.º ano do curso de Licenciatura de Comunicação e Design Multimédia, 2º semestre, sob orientação do docente João Orvalho, foi-nos solicitado a elaboração de um trabalho.
O contexto do nosso projeto aborda o tema do Turismo (particularmente em Portugal), uma área que devido á pandemia tem sofrido diversas alterações.
Com a composição deste projeto final podemos explorar e adquirir novos conhecimentos na área da programação.

## ❔  Aplicação do repositorio

Dormidas nº estadia.json:
   
   	Aceder ao tamanho da tabela de dados de 2019
    Renomear colunas e mostrar colunas importantes
    Quantidade de posições com valores em falta
    Eliminar colunas com dados em falta
    Aceder aos dados que pertencem a Portugal no ano de 2019
    Eliminar linhas com dados em falta

alojamentos2019.cvs:
   
   	Total de informação em falta e posições em que se encontram 
   	Ordenação por ordem alfabética dos nomes dos alojamentos 
   	Identificar as moradias que se enquadram na categoria de motel
 	Localização do motel Alameda

Ano atendimento.csv:
   
   	Visualização do ficheiro como objeto
    Total de atendimentos durante 10 anos
    Média de atendimentos durante 10 anos
    Últimos dois anos de atendimentos
    Gráfico representando atendimentos durante 10 anos

list_Ocupação.json;:
    
    Substituição dos valores no nulos por zero 
    Soma do número de quartos/camas ocupados
    Especificações do hotel com três estrelas
    Descrição da tabela "Ocupação“

preços_1:
   
   	Gráfico representando diferença de preços entre lazer e negócio
    Gráfico global
    Gráfico total de todos os dados

dataset-lugares-publicos-lugares-turisticos.csv:
   
   	Renomeação das colunas das coordenadas
    Eliminar linhas com dados em falta
    Ordenar de forma descrescente todos os dados
    Transformar os valores em strings
    Transformar colunas em valores strings 
    Gráfico de coordenadas



 ## 📖  Fundamentação dos dados

 A recolha de dados devidamente estruturados é crucial para o desenvolvimento do nosso projeto, no entanto grande parte dos dados encontrados tratam-se de dados com fraca qualidade e construídos indevidamente.Posto isto, vimo-nos a ser obrigadas a proceder a uma limpeza dos dados, sendo que estes estavam em mau estado, por exemplo palavras em campos que deveriam ser numéricos e organização por tabela dos dados.

Foi utilizando dois formatos de ficheiro, Json e CSV. O Json são representados como pares de valor-chave num formato semiestruturado, este contém estruturas hierárquicas. O formato CSV são considerados semiestruturados, mas não podem, naturalmente, representar dados hierárquicos ou relacionais.

No caso dos dados “Ano de Atendimento” estes foram importados através de sistema URL, a forma como estavam estruturados os dados fazia com que fosse impossível de ser lida em jupiter, para solucionar o nosso problema passamos á criação de um CSV padrão com os dados que queríamos utilizar corretamente organizados.

Sobre o tema escolhido para este projeto foi realmente difícil encontrar dados que estivessem em formato padrão, o que seria muito benéfico para o bom desenvolvimento deste trabalho.

Para a elaboração da nossa base de dados, importamos ficheiros em CSV padrão e Json, no entanto muitos dos dados encontrados estavam em outros formatos, o que criou alguns problemas. Como por exemplo xlsx, para conseguirmos utilizar estes dados com base no ficheiro "copia de despesas media de turistas" criamos uma tabela ("preços") com os dados e não importamos diretamente o ficheiro.

Departamo-nos com a falta de dados para a execução de exercício relativos á longitude e á latitude, por isso importamos mais dados que não pertencem só a Portugal.


 ## 🧱  Estrutura
 #### Organização repositório:
 
 Dormidas nº estadia.json - contém dados relativos ao número de estadias turísticas no ano de 2019.
 
 alojamento2019.csv - contém dados relativos a alojamentos em 2019 na localidade de Águeda.
 
 Ano atendimento.csv - contém dados extraídos da Câmara Municipal de Águeda que nos fornece o número de atendimentos no posto Turismo do mesmo ao longo de 10 anos.
 
 list_Ocupação.json - contém dados relativos a taxa de ocupação de 4 hotéis com diferentes categorias.
 
 preços_1 - contém dados relativos a despesas turísticas tanto de lazer como de negócios, obtidas através de um inquérito realizado a 1393 hóspedes na cidade de Lisboa.
 
 dataset-lugares-publicos-lugares-turisticos.csv - contém diversos dados de regiões turísticas do mundo, particularmente coordenadas.

 ## 📉  API’s usados – notas técnicas
 Esta base de dados utilizada neste reportório foi grande parte retirada de dados.gov.pt, no entanto utilizamos também dados fornecidos pela Camara Municipal de Agueda.
## 📕  Dicionário de dados
### Dormidas nº estadia.json
<table>
	<tr>
		<td>Nome da coluna</td>
		<td>Significado</td>
		<td>Possiveis valores</td>
	</tr>
	<tr>
		<td>dormidas</td>
		<td>Conjunto de dados de como a informação foi extraída, acerca dos dados de dormidas de 2019</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>dadosDormidas</td>
		<td>Lista dos Dados de 2019</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>dados2019</td>
		<td>Conjunto de dados sobre as informações de dormidas no ano 2019</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>tamanho_tabela_1</td>
		<td>Tamanho tabela dados 2019</td>
		<td>Inteiro</td>
	</tr>
	<tr>
		<td>dados</td>
		<td>Renomeação das colunas</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>dados_1</td>
		<td>Apresenta colunas importantes</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>sem_valores</td>
		<td>Total de dados em falta em dada coluna</td>
		<td>pandas.core.series.Series</td>
	</tr>
	<tr>
		<td>result_sc</td>
		<td>Eliminar colunas com dados em falta</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>rslt_dados2019</td>
		<td>Dados de dormidas em Portugal no ano de 2019</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>result_sl</td>
		<td>Eliminar linhas com valores em falta</td>
		<td>pandas.core.frame.DataFrame</td>
 </table>
 
 
 ### Alojamentos2019.cvs
 <table>
	<tr>
		<td>Nome da coluna</td>
		<td>Significado</td>
		<td>Possiveis valores</td>
	</tr>
	<tr>
		<td>alojamento</td>
		<td>Alojamentos de 2019 de Águeda</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>al_sv</td>
		<td>Soma de todos os valores em falta</td>
		<td>Inteiro</td>
	</tr>
	<tr>
		<td>al_sv_1</td>
		<td>Localização do dados em falta</td>
		<td>Gráfico</td>
	</tr>
	<tr>
		<td>ordem</td>
		<td>Ordenar nomes dos alojamentos por ordem alfabética</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>rslt_alojamentos</td>
		<td>Moradias que se enquadram na categoria motel</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>imgplot</td>
		<td>Moradias que se enquadram na categoria motel</td>
		<td>matplotlib.image.AxesImage</td>
 </table>
 
### Ano atendimento.csv
 <table>
	<tr>
		<td>Nome da coluna</td>
		<td>Significado</td>
		<td>Possiveis valores</td>
	</tr>
	<tr>
		<td>“line”</td>
		<td>Visualização do ficheiro em formato de objeto</td>
		<td>String</td>
	</tr>
	<tr>
		<td>atendimentos</td>
		<td>Atendimentos por ano no posto de Águeda</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>at_10</td>
		<td>Soma do 10 anos de atendimentos</td>
		<td>Inteiro</td>
	</tr>
	<tr>
		<td>media_ at</td>
		<td>Média de atendimentos durante 10 anos</td>
		<td>Inteiro</td>
	</tr>
	<tr>
		<td>ultimos_anos</td>
		<td>Últimos dois anos de atendimentos</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>g_at</td>
		<td>Gráfico representante dos anos de atendimentos</td>
		<td>Gráfico</td>
 </table>

### list_Ocupação.json
 <table>
	<tr>
		<td>Nome da coluna</td>
		<td>Significado</td>
		<td>Possiveis valores</td>
	</tr>
	<tr>
		<td>ocupação</td>
		<td>Conjunto de dados relativos a taxas de ocupação</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>categoria</td>
		<td>Substituição dos valores nulos por 0</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>soma_quartos</td>
		<td>Soma dos quartos ocupados</td>
		<td>Inteiro</td>
	</tr>
	<tr>
		<td>soma_camas</td>
		<td>Soma dos camas ocupados</td>
		<td>Inteiro</td>
	</tr>
	<tr>
		<td>estrelas_3</td>
		<td>Especificações do hotel com 3 estrelas</td>
		<td>pandas.core.series.Series</td>
	</tr>
	<tr>
		<td>d_ocp</td>
		<td>Descrição da tabela “ocupação”</td>
		<td>pandas.core.frame.DataFrame</td>
 </table>
 

### preços_1
 <table>
	<tr>
		<td>Nome da coluna</td>
		<td>Significado</td>
		<td>Possiveis valores</td>
	</tr>
	<tr>
		<td>preços_1</td>
		<td>Conjunto de dados relativos aos preços</td>
		<td>Lista</td>
	</tr>
	<tr>
		<td>gra_preços</td>
		<td>Diferença de preços entre Lazer e Negócio</td>
		<td>Gráfico</td>
	</tr>
	<tr>
		<td>global_1</td>
		<td>Diferença global de Lazer e Negócio</td>
		<td>Gráfico</td>
	</tr>
	<tr>
		<td>total</td>
		<td>Total de todos os dados</td>
		<td>Gráfico</td>
 </table>
 
### dataset-lugares-publicos-lugares-turisticos.csv
 <table>
	<tr>
		<td>Nome da coluna</td>
		<td>Significado</td>
		<td>Possiveis valores</td>
	</tr>
	<tr>
		<td>renomeação_at</td>
		<td>Renomeação das colunas devido a serem nomes estrangeiros</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>coordenadas</td>
		<td>Colunas das coordenadas </td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>c_sl</td>
		<td>Elimina as linhas com falta de dados nas colunas descritas</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>descendente</td>
		<td>Ordenar de forma descendente os dados</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>string_value_1</td>
		<td>Transformar valores em strings</td>
		<td>String</td>
	</tr>
	<tr>
		<td>df</td>
		<td>Transformar colunas em valores strings</td>
		<td>pandas.core.frame.DataFrame</td>
	</tr>
	<tr>
		<td>coordenada_1</td>
		<td>Transformar colunas em valores strings</td>
		<td>Gráfico</td>
 </table>



## 🔎  Bibliografia
https://dados.gov.pt/pt/

https://dados.gov.pt/pt/datasets/r/b9b406ab-bc80-448f-8c47-406f66b4e48a

https://dados.gov.pt/pt/datasets/r/029f7761-d427-404a-a639-a3eb1c83ffd8

https://ckan.sig.cm-agueda.pt/dataset/antendimentos-no-posto-de-turismo-de-agueda/resource/a2abb35b-62b1-4b9f-87b4-5a3a67558626
