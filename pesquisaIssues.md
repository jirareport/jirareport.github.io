# Pesquisa de Issues

A pesquisa de Issues é parecida aos detalhes de períodos em quanto a informação disponibilizada, mas permite uma maior flexibilidade em quanto aos filtros. Podemos selecionar um período maior que os cadastrados (por exemplo, pesquisar desde janeiro/18 até maio/18) para obter uma amostra maior. Pode ser útil na hora de fazer previsões, por exemplo. 

**Nota**: Resaltar que só aparecerão aquelas issues que formam parte de algum período cadastrado, pois para ter uma maior velocidade na realização dos gráficos, são usadas aqueles issues que já foram persistidas na aplicação. Isso significa que se temos três períodos cadastrados por mês (março, abril e maio) e procuramos um período maior de seis meses (de janiero até junho), só vai trazer dados dos três períodos já cadastrados, ignorando o resto.

Para acessar a página de pesquisa de issues, podemos clicar no botão de issues na listagem de projetos.

## Filtros
A tela destaca a parte superior, onde realizamos os filtros desejados:

![Filtros issues](/images/jiratorio-issues-filtros.png)

Os fitros permitidos são:
- Data inicio
- Data fim
- Keys excluidas: Após o primeira filtagem, pode desejar excluir alguma issue da contagem. Por exemplo, aquela issue onde o leadtime foi muito superior ao resto, na hora de fazer previsões pode ser interessante tirar da contagem.
- Sistema: Caso o campo _sistema_ tenha sido configurado, aparecerá um combo para selecionar os diferentes tipos de sistema. Se não houver nada selecionado, vai trazer tudo. O campo permite selecionar mais de um sistema.
- Tamanho da história: Caso o campo _estimativa_ tenha sido configurado, aparecerá um combo para selecionar entre as diferentes estimativas. Se não houver nada selecionado, vai trazer tudo. O campo permite selecionar mais de uma estimativa.
- Épico: Caso o campo _épico_ tenha sido configurado, aparecerá um combo para selecionar entre os diferentes épicos. Se não houver nada selecionado, vai trazer tudo. O campo permite selecionar mais de um épico.
- Issue types: É um combo para selecionar entre os diferentes tipos de issue. Se não houver nada selecionado, vai trazer tudo. O campo permite selecionar mais de um tipo de issue.
- Projeto: Caso o campo _projeto_ tenha sido configurado, aparecerá um combo para selecionar entre os diferentes projetos. Se não houver nada selecionado, vai trazer tudo. O campo permite selecionar mais de um projeto.

O botão filtar vai aplicar os filtros e devolver a pesquisa abaixo do filtro.

## Gráficos
As informações e gráficos gerados nessa tela são os mesmos que aparecem na página [Detalhes do período](/detalhesPeriodo.html). 