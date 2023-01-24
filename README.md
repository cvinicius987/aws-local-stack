# aws-local-stack

### Container LocalStack

```shell
docker run -d -p 4566:4566 -e SERVICES=sqs localstack/localstack:0.12.2
```

### Listando os serviços ativos

```shell
http://localhost:4566/health
```

### Referências

https://docs.aws.amazon.com/cli/latest/reference/s3/#
https://docs.aws.amazon.com/cli/latest/reference/s3api/