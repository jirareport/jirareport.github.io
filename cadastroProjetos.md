# Cadastro de projetos

A tela de cadastro de projetos é [http://localhost:8080/projects](http://localhost:8080/projects). Para cadastrar um produto novo, pode seguir as instruções da [configuração inicial](/startConfig.html). Uma vez cadastrado o projeto, ele vai aparecer na listagem:

![Listagem de períodos](/images/jiratorio-periodos-listagem.png)

## Alterar configurações
Quando já temos nosso projeto cadastrado, as vezes sentimos a necessidade de fazer alguma alteração nas configurações. Basta clicar no botão de **Configurações** e aparecerá a tela de configuração preenchida com os valores salvos no banco.

## Feriados
Podemos configurar os feriados clicando no botão. Isso permite subtrair aqueles dias de segunda a sexta que não foi trabalhado (feriado nacional, emenda, feriado local, etc)

![Listagem de feriados](/images/jiratorio-feriados-listagem.png)

Para criar feriados, temos duas opções:
- Criar um novo: Possibilidade de criar um dia de ferias especifico (por exemplo, feriado local da cidade)
- Importar Feriados: Usando a api de feriados, conseguimos importar os feriados e não precisamos de digitar.

## Configurações de lead time
Podemos configurar lead times alternativos (ou cycle times) para realizar comparações. Por exemplo, tempo de desenvolvimento, tempo desde backlog até entrega em prod, ou tempo de UI/UX. Se você quiser comprar o leadtime original com qualquer outro, precisa ser cadastrado novamente nessa opção.

![Configuração de leadtime](/images/jiratorio-leadtimes.png)

## Períodos
Clicando nessa opção, acessamos a página de [Cadastro de períodos](/cadastroPeriodos.html).

## Issues
Clicando nessa opção, acessamos a página de [Pesquisa de issues](/pesquisaIssues.html).

