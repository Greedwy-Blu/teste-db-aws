# teste-db-aws

aws dynamodb create-table \
    --table-name Funcionarios \
    --attribute-definitions \
        AttributeName=ID,AttributeType=S \
    --key-schema \
        AttributeName=ID,KeyType=HASH \
    --provisioned-throughput \
        ReadCapacityUnits=5,WriteCapacityUnits=5


aws dynamodb put-item \
    --table-name Funcionarios \
    --item '{
        "ID": {"S": "001"},
        "Nome": {"S": "João Silva"},
        "Cargo": {"S": "Desenvolvedor"},
        "Salario": {"N": "5000"}
    }'


aws dynamodb put-item \
    --table-name Funcionarios \
    --item '{
        "ID": {"S": "002"},
        "Nome": {"S": "Maria Oliveira"},
        "Cargo": {"S": "Gerente"},
        "Salario": {"N": "8000"}
    }'

aws dynamodb put-item \
    --table-name Funcionarios \
    --item '{
        "ID": {"S": "003"},
        "Nome": {"S": "Pedro Souza"},
        "Cargo": {"S": "Analista de Dados"},
        "Salario": {"N": "6000"}
    }'
