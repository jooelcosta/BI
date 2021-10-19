Foi proposto um desafio pelo mentor do curso de Power BI, Leonardo Karpisnki.

O desafio era obter os dados de uma planilha excel e fazer as transformações necessárias e obter insisghts.

O resultado pode ser visto através do link abaixo:

[Desafio Kick Start](https://app.powerbi.com/view?r=eyJrIjoiMzhiODk2ZjktYzQ5NC00NTY4LTk1YzEtMzBlMDJjOTFiOTU2IiwidCI6ImFmMTJhMmZkLTI0NjgtNDA1OS1hNTFhLTYyZmRhM2U2OTBiNSJ9&pageName=ReportSection047258e706d600e79a61) 


--![](https://i.ibb.co/j8x063m/pbi.png)

Informações detalhadas:

**ETL**

*Uma visão geral de como os dados estavam dispostos na planilha:*

![](https://i.ibb.co/kXQy9bq/base1.png)
![](https://i.ibb.co/T8J6kBq/base2.png)
![](https://i.ibb.co/7bYLc4x/base3.png)
![](https://i.ibb.co/jh61w7b/base4.png)

**Importando a base de dados**

- A importação foi feita como a imagem abaixo;
- A tabela produtos não foi importada pois não estava no formato ideal para se trabalhar no Power BI.
![image](https://i.ibb.co/1bHzVJ8/navigator.png)
- Verificando que as Tabela2, 3 e 4, continha todas as informações dos produtos;
- A Tabela4 foi renomeada para dProdutos.

**Dimensão Produtos**
*Para manter todas as informações de produtos em uma única tabela, a tabela Imagem Produtos foi mesclada com a Tabela4 e expandida somente a coluna de Imagem ficando dessa forma:* 

![image](https://i.ibb.co/tmmgSMx/mescla-consulta.png)

Obs.: A tabela Imagem Produtos teve a opção de carregar no modelo desabilitada, mas mantendo as atualizações de dados.
Para manter uma ordem dos ID’s de produtos na tabela a Tabela4 foi escolhida como a principal para que as Tabela2 e 3 fossem acrescentadas, respectivamente.
Obs.: A Tabela2 e 3 tiveram a opção de carregar no modelo desabilitadas, mas mantendo as atualizações de dados.

![image](https://user-images.githubusercontent.com/45804263/137969695-c1a6a684-ebf8-4cce-ab32-1c3078ac0069.png)









