# Projetos-em-PySpark
Explorando PySpark
# from pyspark.sql import SparkSession
from pyspark.sql.functions import col

# Criando a sessão do Spark
spark = SparkSession.builder \
    .appName("ExemploPySpark") \
    .getOrCreate()

# Criando uma lista de dados
dados = [(1, "Alice", 25), (2, "Bob", 30), (3, "Carol", 22)]

# Definindo os nomes das colunas
colunas = ["id", "nome", "idade"]

# Criando o DataFrame
df = spark.createDataFrame(dados, colunas)

# Exibindo o DataFrame
df.show()
