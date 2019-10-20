# Codigo da palestra "Criando aplicações serverless com PHP"

Este repositorio contém o codigo usado na palestra **Criando 
aplicações serverless com PHP**. O código consiste em duas pastas:

- simple-helloworld: Primeiro exemplo apresentado de uma aplicação HTTP simples
 de hello world. 
- simple-routing: Segundo exemplo apresentado de uma aplicação simples
de roteamento.

Os slides estão disponíveis no speakerdeck: [https://speakerdeck.com/omarkdev/criando-aplicacoes-serverless-com-php](https://speakerdeck.com/omarkdev/criando-aplicacoes-serverless-com-php)

## Configurando

Antes de começar a usar qualquer exemplo, você precisa configurar
o serverless framework na sua máquina, para configurar siga as instruções:

Primeiramente você precisa ter instalado na sua máquina o Node e o NPM.

Tendo as dependências instaladas, instale o serverless na sua máquina:

```
npm i -g serverless
```

Agora é necessário configurar as credenicias da AWS no serverless (cada provedor
tem sua maneira de configurar, aqui usaremos a AWS apenas como exemplo):

```
serverless config credentials \
  --provider aws \
  --key $AWS_ACCESS_KEY_ID \
  --secret $AWS_SECRET_ACCESS_KEY
```

**Obs**: As variaveis de ambiente `@AWS_ACCESS_KEY_ID` e `$AWS_SECRET_ACCESS_KEY` vocẽ 
deve substituir por suas chaves.

Pronto, sua máquina está configurada para executar o serverless framework.

## Como usar

Para você usar, independente de qual exemplo, basta acessar a pasta e seguir os seguintes passos:

Instalar as dependencias do PHP:
```
composer install
```

Com as dependencias instalas sua aplicação está pronta para usar e fazer deploy. Testando
localmente:

```
php -S localhost:8000 index.php
```

E acessar `http://localhost:8000`.

## Deployando

Para fazer o deploy, primeiro você precisa ter configurado o serverless
framework na sua máquina e instalado as dependências. Com isso previamente feito
basta digitar:

```
serverless deploy
```

O serverless framwork irá fazer deploy da sua aplicação.

## Considerações

Este repositório tem a principal finalidade de conter o código
apresentado na palestra para que possa ser consultado e testado
posteriormente.

Caso você tenha assistido a palestra e queira lembrar dos passos apresentados
você pode olhar o histórico de commits, pois o histórico segue a ordem do conteúdo
apresentado durante a palestra.
