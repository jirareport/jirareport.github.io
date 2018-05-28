# Detalhes do Período

Quando entramos no detalhe de um período, o primeiro que vemos é a seguinte tela:

![Detalhe de periodo](/images/jiratorio-periodo-issues-listagem.png)

Basicamente, vemos dois cards grandes com o leadtime médio e o número de histórias do período. E a continuação, um grupo de abas que pode ser maior ou menor em função da [configuração do projeto](/startConfig.html#novo-projeto), como estimativa, sistema, projeto, etc.

## Issues
Aparece a lista de issues finalizadas, segundo a configuração do projeto, nesse período. Alguns campos aparecem só se estão configurados. Se clicamos acima da issue, aparece o detalhe da mesma:

![Detalhe da issue](/images/jiratorio-periodo-issue-details.png)

Nela aparece o tempo em cada coluna, expressado em dias. Esse tempo por coluna é bom lembrar que é sempre arredondado para cima. Se uma issue passou por uma coluna só 5 minutos, na listagem vai aparecer 1. Isso é porque o que realmente queremos mostrar aqui é se houve alguma coluna que onerou especialmente.

Também aparece, caso tiver configurado, uma comparativa de leadtimes adicionais.

## Histograma de leadtime
Olhando para o leadtime principal, o histograma é útil principalmente para realizar estimativas. 

![histograma](/images/jiratorio-periodo-histograma.png)

As vezes, podemos desejar analisar um período maior para ter mais insumos. Como seria isso possível? Acessando a página de [Pesquisa de issues](/pesquisaIssues.html).

## Contagem de estimativa
O gráfico mostra a distribuição de histórias por tamanho.

![Estimativa](/images/jiratorio-periodo-estimativa.png)

Só vai aparecer se o campo estimativa estiver configurado.

## Lead time médio por tamanho de história
O gráfico mostra a comparativa de Lead time médio por tamanho de história.

![Estimativa](/images/jiratorio-periodo-leadtime-estimativa.png)

Só vai aparecer se o campo estimativa estiver configurado.

## Lead time/histórias por sistema
O gráficos mostram a distribuição por número de histórias e a comparativa de Lead time médio por sistema.

![Sistema](/images/jiratorio-periodo-leadtime-sistema.png)

Só vão aparecer se o campo sistema estiver configurado.

## Lead time/histórias por tipo de issue
O gráficos mostram a distribuição por número de histórias e a comparativa de Lead time médio por tipo de issue.

![Sistema](/images/jiratorio-periodo-tipo-issue.png)

## Lead time/histórias por projeto
O gráficos mostram a distribuição por número de histórias e a comparativa de Lead time médio por projeto.

Só vão aparecer se o campo projeto estiver configurado.

## Lead Times
Mostra a comparativa entre os diferentes leadtimes adicionais configurados por história.

![Leadtimes](/images/jiratorio-periodo-issue-comparativas.png)

Só vão aparecer se houver leadtimes adicionais configurados.

### Flexibilidade
Os dados por período são fixos. Não permite filtros mais específicos. Para isso, existe a página de [Pesquisa de issues](/pesquisaIssues.html).