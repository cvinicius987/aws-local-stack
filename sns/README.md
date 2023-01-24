
Conectando através do AWS CLI ao Serviço de filas SQS do LocalStack

## Operações no Local Stack

#### Criando SNS Topics

```shell
aws --endpoint-url=http://localhost:4566 sns create-topic --name topic_tests
````

#### Listando os Topics SNS

```shell
 aws sns list-topics --endpoint-url http://localhost:4566
```