# Configuração inicial
Para logar na aplicação, basta entrar na url [http://localhost:8080/login](http://localhost:8080/login) e digitar o seu usuário e senha do Jira.

![login](/images/jiratorio-login.png)

##Problemas de autenticação?
Caso seja apresentada uma mensagem parecida com a mensagem abaixo, use o link a seguir para corrigir
_javax.net.ssl.SSLHandshakeException: sun.security.validator.ValidatorException: PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target_


https://confluence.atlassian.com/kb/unable-to-connect-to-ssl-services-due-to-pkix-path-building-failed-779355358.html

##Problemas de certificado?
https://confluence.atlassian.com/kb/how-to-import-a-public-ssl-certificate-into-a-jvm-867025849.html#HowtoimportapublicSSLcertificateintoaJVM-commandline


## Novo projeto
Depois de logar, clique no botão NOVO BOARD e será redirigido para a página que irá listar os projetos disponíveis. Selecione o projeto desejado e clique em salvar. 


Uma vez encontrado, clique em salvar. Vai aparecer a tela inicial de configuração:

![Configuração de Projeto](/images/jiratorio-config-project.png)

Os campos que podemos preencher são os seguintes:
- Nome: Indica o nome do projeto.
- Coluna inicial: Indica qual é a coluna/estado onde o seu leadtime começa a contar. Tem uns botões embaixo com algumas sugestões de colunas.
- Coluna final: Indica qual é a coluna/estado onde o seu leadtime para de contar. Tem uns botões embaixo com algumas sugestões de colunas.
- Fluxo ordenado de colunas: Indica o fluxo das suas colunas/estados de forma sequencial. É usado para contemplar histórias que não passaram pela coluna inicial/final (por exemplo, passou de _backlog_ à _desenvolvimento_ sem passar por _analise_).
- Tipo de issues à serem ignorados: Indica se há algum tipo de issue à ser desconsiderado. Pode ser usado para não avaliar os épicos, por exemplo. Se não informar nada, usará todos os issues existentes.
- Campo de Épico: Indica o campo usado nas issues para indicar o épico ao que pertence. Se não for informado, será desconsiderado nos cálculos.
- Campo de tamanho/estimativa: Indica o campo usado para indicar as estimativas (por exemplo, P,M,G). Se não for informado, será desconsiderado nos cálculos.
- Campo de sistemas: Indica o campo usado nas issues para indicar o sistema. (Por exemplo, _monolítico_, _microserviço_, _script_, _outros_). Se não for informado, será desconsiderado nos cálculos.
- Campo de projeto: Indica o campo usado nas issues para indicar o projeto. (Por exemplo, _faturamento_, _cadastro de usuários_, _Nota fiscal_)

Finalmente, podemos salvar o projeto. 

Após salvar, entraremos na tela de Cadastro de períodos do projeto.

Para cadastro de projetos, veja a a página [Cadastro de projetos](/cadastroProjetos.html).
