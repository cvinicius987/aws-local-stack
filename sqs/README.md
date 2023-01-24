
Conectando através do AWS CLI ao Serviço de filas SQS do LocalStack

## Container LocalStack

```shell
docker run -d -p 4566:4566 -e SERVICES=sqs localstack/localstack:0.12.2
```

## Operações no Local Stack

#### Criando SQS Queues

```shell
aws --endpoint-url=http://localhost:4566 sqs create-queue --region us-east-1 --queue-name queue_sqs_test
````

#### Listando as Queues SQS

```shell
 aws sqs list-queues --endpoint-url http://localhost:4566
```