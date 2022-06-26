# kafka-windows-configuracoes

rodar kafka (versão binária, projeto já compilado e configurado)

cd C:\kafka-binario\kafka\bin\windows

zookeeper-server-start.bat ../../config/zookeeper.properties

kafka-server-start.bat ../../config/server.properties

# Criando tópico (nova aba):

kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic LOJA_NOVO_PEDIDO

# Listar topicos (nova aba):

kafka-topics.bat --list --bootstrap-server localhost:9092

# Produtor (nova aba):

kafka-console-producer.bat --broker-list localhost:9092 --topic LOJA_NOVO_PEDIDO
>pedido,50reais

# Consumidor (nova aba):
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic LOJA_NOVO_PEDIDO

# Consumir desde o início:

kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic LOJA_NOVO_PEDIDO --from-beginning
