# Cadastro de perídos

Na página inicial de cadastro de períodos, aparece uma seleção de data inicial e final com um botão de salvar e, abaixo, a listagem de períodos cadastrados.

![Listagem de periodos](/images/jiratorio-periodos-listagem.png)

## Novo período
Para cadastrar um novo período é simples, só precisamos especificar a data inicial e data final do período e clicar em salvar. O JiraTório vai acessar ao jira e recuperar aquelas issues que finalizaram, segundo a definição de coluna inicial especificada no [cadastro do projeto](/startConfig.html#novo-projeto). Também usará as demais configurações como campo de estimativa, campo de sistema, [leadtimes configurados](/cadastroProjetos.html#configuraes-de-lead-time), [feriados cadastrados](/cadastroProjetos.html#feriados) para realizar os cálculos necessários. Uma vez salvado o período, ele aparece na listagem. As issues são importadas e não é mais consultado o jira se não for solicitado (ver abaixo [atualizar](/cadastroPeriodos.html#atualizar-perodo)). 
É aconselhável cadastrar períodos fixos de tempo (por semana, por mês), pois os gráficos gerados nas abas ao lado da _Listagem_ realizam comparativa entre períodos, e não faz sentido comparar meses com semanas, por exemplo.

## Listagem
Na listagem, temos as seguintes informações:
- Período cadastrado
- Leadtime: Cálculo de leadtime em dias, usando as colunas configuradas como inicio e final no [cadastro do projeto](/startConfig.html#novo-projeto), assim como descontando [feriados](/cadastroProjetos.html#feriados) e finais de semana.
- Histórias: Número de histórias que finalizaram nesse período, isso é o throughtput
- Ações: Ver a continuação.

## Remover período
Caso cadastrar um período errado, existe a possibilidade de remové-lo. Basta clicar no botão remover das ações, e após confirmação, o período é removido.

## Atualizar período
Pode acontecer que o período cadastrado está certo, mas você não configurou o sistema dentro do [cadastro do projeto](/startConfig.html#novo-projeto), ou adicionou um [Leadtime novo](/cadastroProjetos.html#configuraes-de-lead-time), ou simplesmente esqueceu um [feriado](/cadastroProjetos.html#feriados). Para não precisar remover e adicionar de volta, basta em clicar em atualizar.

## Detalhe do período
Os detalhes do período podem ser consultados no seguinte [link](/detalhesPeriodo.html)

## Gráficos
A continuação, vamos descrever os gráficos disponíveis para comparar os períodos cadastrados.

### LeadTime
O gráfico compara os diferentes leadtimes de forma gráfica e ordenada por datas.

![Periodos-leadtime](/images/jiratorio-periodos-leadtime.png)

Colocando o mouse acima da coluna, aparece o valor exato do leadtime.

### Contagem de histórias
O Gráfico mostar a comparativa de throughtput (histórias por período) ordenado por data:

![Periodos-historias](/images/jiratorio-periodos-historias.png)

### Contagem de histórias por estimativa
O gráfico é parecido à contagem de histórias, porém quebrado por estimativa.

![Periodos-estimativa](/images/jiratorio-periodos-estimativa.png)

Se no [cadastro do projeto](/startConfig.html#novo-projeto) não foi especificada a coluna de estimativa, a aba não vai aparecer.

### Lead times
O gráfico mostra a comparativa entre os diferentes [leadtimes adicionais configurados](/cadastroProjetos.html#configuraes-de-lead-time). 

![Periodos-comparativa](/images/jiratorio-periodos-comparativa.png)
 
Se você quer comparar com o leadtime principal, ele precisa ser cadastro de novo como leadtime adicional. Caso não cadastre nenhum leadtime, a aba não vai aparecer.
