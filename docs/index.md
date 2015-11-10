FARMS significa Ferramenta de Apoio à Revisão e ao Mapeamento Sistemático e
trata-se de uma aplicação web que visa facilitar o trabalho da comunidade
acadêmica em seus projetos de pesquisa, fornecendo uma solução colaborativa para
o levantamento das bibliografias a respeito de um determinado tema, em específico
, a realização de revisões sistemáticas e mapeamentos sistemáticos.

[TOC]

# Começando

A priore, nosso desejo é disponibilizar um serviço online totalmente gratuito
, porém a ferramenta ainda não está pronta para ser disponibilizada à comunidade
acadêmica. Portanto, se você não é um desenvolvedor da área de TI, talvez os
conteúdos aqui documentados não signifiquem muita coisa para você. Mas não se
preocupe, assim que a ferramenta estiver disponível não somente para os
desenvolvedores, iremos escrever todo o material necessário para que você possa
tirar maior proveito de todas as funcionalidades.

Você precisará dos seguintes itens:

* Arquivos da aplicação web e do webservice (links mais adiante).
* Ter o Java instalado em sua máquina. [Download](http://www.java.com/)
* Apache Tomcat (recomendamos a versão 8). [Download](http://tomcat.apache.org/download-80.cgi)
* PostgreSQL. [Download](http://www.postgresql.org/download/)

___

## Instalação

1. Obtenha os códigos da [aplicação web](https://github.com/farms/farms-webapp)
em nosso repositório no GitHub no link a seguir:
[farms-webapp](https://github.com/farms/farms-webapp/archive/master.zip).
Ou clone por meio do git através da linha de comando utilizando
``git clone https://github.com/farms/farms-webapp.git``

2. Também obtenha os códigos do [webservice](https://github.com/farms/farms-webservice)
no link a seguir: [farms-webservice](https://github.com/farms/farms-webservice/archive/master.zip).
Ou clone por meio do git utilizando o comando ``https://github.com/farms/farms-webservice.git``

3. Nos arquivos do webservice, navegue até o diretório ``/src/main/resourcers/META-INF/``
e abra o arquivo ``persistence.xml``. Em seguida edite-o alterando as linhas a
seguir substituindo os valores 'root' pelas suas credenciais de acesso ao
PostgreSQL.

```xml
<property name="javax.persistence.jdbc.user" value="root" />
<property name="javax.persistence.jdbc.password" value="root" />
```
___

## Executando

Após feito o download dos arquivos e inserido as credenciais de acesso ao banco
de dados você poderá executar o projeto.

1. Crie uma base de dados com o nome Farms em seu PostgreSQL.

2. Execute o WebService. Neste momento, as tabelas deverão ser automagicamente
criadas em seu banco de dados.

3. Inicie o WebApp através do servidor Tomcat.

4. Pronto! Agora basta acessar o endereço no qual o Apache Tomcat está executando
a aplicação. Normalmente localhost:8080.