
Conectando através do AWS CLI ao Serviço de topics SNS do LocalStack

## Operações no Local Stack

#### Criando SNS Topics

```shell
aws --endpoint-url=http://localhost:4566 sns create-topic --name topic_name
````

#### Listando os Topics SNS

```shell
 aws sns list-topics --endpoint-url http://localhost:4566
```

#### Listando Subscriptions SNS

```shell
 aws sns list-subscriptions  --endpoint-url=http://localhost:4566
```

#### Adicionando o SNS como subscribe de uma Queue SQS

```shell
aws --endpoint-url=http://localhost:4566 sns subscribe --topic-arn arn:aws:sns:us-east-1:000000000000:topic_name --protocol sqs --notification-endpoint http://localhost:4566/000000000000/queue_name
```

#### Enviando mensagens ao topic SNS

```shell
aws sns publish  --topic-arn arn:aws:sns:us-east-1:000000000000:topic_name --message 'Message content!' --endpoint-url=http://localhost:4566
```