# Criando um banco de dados

create database {nome_do_banco};

Esse comando podemos utilizar para criar o banco de dados.

# Criando um banco de dados com um assitente

No MysqlWorkbenq podemos clicar com o botão direito e logo em seguida, create schema. E podemos seguir, informando quais as regras que desejamos no nosso banco de dados.

Assim, ela nos ajuda a agilizar na criação de comandos SQL. 


# Apagando um banco de dados

Para deletar um banco de dados podemos passar o seguinte comando: 

drop database {nome_do_banco}

E logo em seguida, caso exista o banco, o mesmo vai ser deletado. 

No MysqlWorkbenq podemos clicar com o botão direito em cima do banco também e realizar a ação de apagar o banco de dados.

## Tipos de dados

Quando definimos que uma tabela vai ter um tipo, esse valor não pode ser alterado. 
Logo, todos os dados dessa mesma coluna tem que ser do mesmo tipo.

O tipo, está diretamente relacionado a quantidade de espaço que vamos gastar para armazenar o mesmo no banco de dados.


## Tipos Numericos


# INT

TINYINT - 1 Bytes / 255 (Numero de caracteres aceitos)
SMALLINT - 2 Bytes / 65535 (Numero de caracteres aceitos)
MEDIUMINT - 3 Bytes / 16777215 (Numero de caracteres aceitos)
INT - 4 Bytes / 4294967295  (Numero de caracteres aceitos)
BIGINT - 8 Bytes / 2x-E64-1 (Numero de caracteres aceitos)

Logo, esses são os tipos e tamanhos que os dados numeros ocupam e podem ser declarados dentro de um banco de dados.

*Obs: Contem uma imagem contendo as informações mais detalhadas sobre os valores.*

*UNSIGNED*
Não permite sinal de um numero, por isso o conjunto de valores validos aumenta.

# Ponto flutuante 

Significa que o mesmo faz um arredondamento, quando o numero de casas decimais for maior do que o permitido no banco. 

Ex:

Os 2 que temos são o *float & double*, diferença apenas de armazenamento.

*Float: 4bytes*

*Double: 8bytes*

O double faz um arredondamento mais preciso, então quando queremos algo mais preciso utilizamos o double.

## Fixos 

Temos os tipos *Decimal & Numeric*, ambos são iguais. Não importa muito, ele na verdade é definido em tamanho de numeros podem ter e ele pode ter no maximo: 65 digitos.

Ele não vai fazer uma aproximação, ele vai adicionar o exato numero que foi passado. Ex:

Se declararmos um campo DECIMAL(5,2) iremos poder armazenar valores somente entre -999,99 ~ 999,9.

E com o numero mais de digitos 65. 

# BIT 


Tamanho de até 64 bits

Exemplo: 
BIT(1) - Pode ser 1 ou 0.

BIT(2) - Pode ser 01, 10, 00, 11.

Utilizados para tipo logico, sendo 1 =  true, 0 = false.

## Atributos para campos numericos

*Signed & UNSIGNED* -  Vai possuir ou não sinal no numero. ( negativo ou não.) 

*ZeroFill* - Preenche com 0 os espaços.
Ex: INT(4) Se armazenar o valor 5, ele vai armazenar 0005. 

*AUTO_INCREMENT* - Sequencia auto incrementada, ex: 0,1,2,3,4...

Normalmente não inserimos dados, e deixamos que o propio banco adicione, exemplo: ID. 

Erros de OUT OF RANGE - Vai ocorrer quando os limites estourarem.


## Data e Hora

*Date* - 1000-01-01 até 9999-12-31

*Datetime* - 1000-01-01 00:00:00 até 9999-12-31 23:59:59

*TimeStamp* -  1970-01-01 00:00:01 UTC até 2038-01-19 UTC

*Time* - -838:59:59 e 839:59:59

*Year* - 1901 - 2155 ( Pode ser expresso ou formato 2 ou 4 dígitos)

## Tipo String

*CHAR* - Cadeia de caracteres com valor fixo (0 a 255);


*VARCHAR* - Cadeia de caracteres com valores variados (de 0 a 255)

Ex: 

Char(4) - "aa" - "  aa"

Ele preenche com vazio quando não passamos os suficientes.

Varchar(4) - "aa" - "aa"

Ele armazena só o que foi passados.

*Binary* - Cadeia de caracteres com valores fixos (0 a 255). Expressos em binarios.

*VarBinary* -  Cadeia de caracteres com valor variado ( de 0 a 255). Expressos em binarios.


Diferença que ao invez de gravar caracteres, gravamos os bytes.


*Blob* - Binario longo. Podemos ter:

Tinyblob
Blob
Mediumblob
longblob

*Text* - Texto longo. Podemos ter:

TinyText 
Text
Mediumtext
LongText

*Enum*

- Permite armazenar uma lista pré definidas de valores.

Ex: 

Size ENUM('x-small', 'small', 'medium', 'large','x-large')

Dizemos que só podemos guarda uma dessas 5 opções.

## Atributos da String

*SET & COLLATE* - Que tipo de conjunto de caracteres serão suportados.


## Spacial 

*Geometry* - Representa área.
*Point*
*LINESTRING*
*POLYGON* - Representa área.


## Criando tabelas.