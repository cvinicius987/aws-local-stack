
Conectando através do AWS CLI ao Serviço S3 do LocalStack, podendo ser utilizado o *aws s3* ou *aws s3api*

## Operações no Local Stack

#### Criando um Bucket S3

```shell
aws s3 mb s3://local-bucket --endpoint-url http://localhost:4566
```

#### Listando Buckets

```shell
aws s3 ls --endpoint-url http://localhost:4566 
```

#### Listando Arquivos em um Bucket

```shell
aws s3 ls s3://local-bucket --endpoint-url http://localhost:4566 
```

#### Enviando um Arquivo ao Bucket S3

```shell
aws s3api put-object --bucket local-bucket --key file.txt --body file.txt --endpoint-url http://localhost:4566
```

#### Excluindo um Bucket

```shell
aws s3 rb s3://local-bucket2 --endpoint-url http://localhost:4566 
```