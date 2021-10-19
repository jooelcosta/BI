Foi proposto um desafio pelo mentor do curso de Power BI, Leonardo Karpisnki.

O desafio era obter os dados de uma planilha excel e fazer as transformações necessárias e obter insisghts.

O resultado pode ser visto através do link abaixo:

[Desafio Kick Start](https://app.powerbi.com/view?r=eyJrIjoiMzhiODk2ZjktYzQ5NC00NTY4LTk1YzEtMzBlMDJjOTFiOTU2IiwidCI6ImFmMTJhMmZkLTI0NjgtNDA1OS1hNTFhLTYyZmRhM2U2OTBiNSJ9&pageName=ReportSection047258e706d600e79a61) 

Informações detalhadas:

**ETL**

*Uma visão geral de como os dados estavam dispostos na planilha:*

![image](https://user-images.githubusercontent.com/45804263/137970140-04e88e25-32ee-463f-9287-de45797298c5.png)
![image](https://user-images.githubusercontent.com/45804263/137970190-19fc02eb-1895-4a92-acd3-c196e5716fce.png)
![image](https://user-images.githubusercontent.com/45804263/137970211-dbc64187-235b-4dcc-b398-f4c671886b19.png)
![image](https://user-images.githubusercontent.com/45804263/137970226-c4e3fa42-f790-4ed7-9ff1-e78c82975917.png)

**Importando a base de dados**

- A importação foi feita como a imagem abaixo;
- A tabela produtos não foi importada pois não estava no formato ideal para se trabalhar no Power BI.
![image](https://user-images.githubusercontent.com/45804263/137970257-eeddfc93-3a86-4328-b7d3-076b0cb05848.png)
- Verificando que as Tabela2, 3 e 4, continha todas as informações dos produtos;
- A Tabela4 foi renomeada para dProdutos.

**Dimensão Produtos**

*Para manter todas as informações de produtos em uma única tabela, a tabela Imagem Produtos foi mesclada com a Tabela4 e expandida somente a coluna de Imagem ficando dessa forma:* 

![image](https://user-images.githubusercontent.com/45804263/137970317-9c7a832c-26c1-4205-987a-1ea007758e5c.png)

Obs.: A tabela Imagem Produtos teve a opção de carregar no modelo desabilitada, mas mantendo as atualizações de dados.
Para manter uma ordem dos ID’s de produtos na tabela a Tabela4 foi escolhida como a principal para que as Tabela2 e 3 fossem acrescentadas, respectivamente.

![image](https://user-images.githubusercontent.com/45804263/137970674-7b2d44b0-dc13-4aef-a749-1dafcd7f6128.png)


Obs.: A Tabela2 e 3 tiveram a opção de carregar no modelo desabilitadas, mas mantendo as atualizações de dados.

![image](https://user-images.githubusercontent.com/45804263/137969695-c1a6a684-ebf8-4cce-ab32-1c3078ac0069.png)

**Fato Vendas**

*A tabela Vendas veio inicialmente dessa forma.
Para não afetar a performance com steps desnecessárias, Promoted Header e Changed Type que são criadas automaticamente após a importação das tabelas, foram excluídas.*

![image](https://user-images.githubusercontent.com/45804263/137970073-b6755af8-0f37-4d4f-be29-d4d4124558fe.png)

*Finalizando a tabela Vendas, o resultado parcial é esse.*

![image](https://user-images.githubusercontent.com/45804263/137970385-1ceee731-0155-46f9-a140-230d8aa41f9c.png)

*Para uma melhor análise de lojas a coluna Loja foi aproveitada para que fosse criada uma dimensão.*

**Dimensão Lojas**

*Foi feito a cópia da tabela Vendas e aplicada as steps necessárias*

![image](https://user-images.githubusercontent.com/45804263/137970966-e5a7c8d4-5aaa-41fe-9d5d-a6ff38135224.png)

Obs.: Após criação da dLoja, a coluna loja na tabela Vendas foi alterada para manter apenas o ID.

**Atendendo demanda do business case**

No business case é pedido o seguinte:

*“Como você estimaria a quantidade de vendas sabendo que o mesmo cliente
pode comprar mais de um produto na mesma venda? Lembrando que não
temos a informação de qual cliente comprou.”*

Pensando nisso, foi criado uma coluna que agrega idades: FaixaEtaria.
Foi feito dessa forma:
![image](https://user-images.githubusercontent.com/45804263/137971124-79f64975-3aaa-4727-a843-d97eff0ebc86.png)

**Dimensão Tempo**

*Para um melhor controle de datas e filtros, foi criada a dimensão de tempo usando a função List.Dates e deixando de forma dinâmica. Pegando sempre o início do menor ano da tabela de venda até o fim do maior ano.*

![image](https://user-images.githubusercontent.com/45804263/137971207-66ee7096-ef37-4da6-a601-e67e62346368.png)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Relatorio**

**Pagina Inicial**

![image](https://user-images.githubusercontent.com/45804263/137971341-0e545af9-a626-410e-bec1-3562d94f3bd9.png)

**Análise de Vendas**

- Menu de navegação entre páginas
- Cartões totalizadores
- Indicadores como % YoY do Faturamento
- Ticket Médio
- Fácil troca de análise do Top3 por loja ou produto
- Fácil análise de vendas por loja, por cidade e ticket médio por categoria

![image](https://user-images.githubusercontent.com/45804263/137971678-de89e226-42c3-4522-a2b2-da69c3801988.png)

**Análise de Devoluções**

- Menu de navegação entre páginas
- Tooltip com imagem do produto e outras informações
- Simulador de taxa de devolução

![image](https://user-images.githubusercontent.com/45804263/137971910-3b0cde0b-6b07-4570-884c-e7f455aa04ca.png)

**Simulador**
- De acordo com a porcentagem definida, é mostrado o valor do novo faturamento e o lucro extra do produto.

![image](https://user-images.githubusercontent.com/45804263/137971798-a17b970c-7ca4-434d-a066-65f7b0646993.png)
