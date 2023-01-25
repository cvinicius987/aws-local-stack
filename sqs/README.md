
Conectando através do AWS CLI ao Serviço de filas SQS do LocalStack

## Operações no Local Stack

#### Criando SQS Queues

```shell
aws --endpoint-url=http://localhost:4566 sqs create-queue --region us-east-1 --queue-name queue_sqs_test
````

#### Listando as Queues SQS

```shell
 aws sqs list-queues --endpoint-url http://localhost:4566
```

#### Consumindo mensagens

```shell
aws sqs receive-message --queue-url http://localhost:4566/000000000000/queue_sqs_test --endpoint-url=http://localhost:4566
```