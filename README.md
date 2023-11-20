# Criando o Ambiente Spark no Linus

Primeiro é necessario criar o ambiete virtual venv no computador. Para isso, abra o terminal com "Ctrl + J" e em seguida use os seguintes comandos:

    sudo apt update; sudo apt upgrade; sudo apt install python3.9; python3.9 -m venv venv; source venv/bin/activate

Feito isso, o ambiente spark deve ser configurado da seguinte maneira:

O Spark tem uma particularidade, pois precisa ter o Java instalado na máquina para funcionar. Para verificarmos se ele está instalado, podemos executar o seguinte comando no terminal:

    java -version

Se tivermos o Java na máquina, nos será retornada a versão existente. Caso contrário, o sistema avisará que não reconhece este comando indicando que o Java não está instalado. Para instalá-lo, podemos usar o comando apt-get install openjdk-8-jdk-headless -qq.

    apt-get install openjdk-8-jdk-headless -qq

Caso ele retorne um erro, significa que não estamos utilizando o comando de administrador, então basta adicionar sudo ao início do comando.

    sudo apt-get install openjdk-8-jdk-headless -qq

## Preparando o ambiente: instalando Spark
De volta no terminal do VSCode, instale as seguintes bibliotecas:

    pip install pyspark==3.3.1

    wget https://archive.apache.org/dist/spark/spark-3.1.3/spark-3.1.3-bin-hadoop3.2.tgz

    tar -xvzf spark-3.1.3-bin-hadoop3.2.tgz

    export SPARK_HOME=/home/eugenio/Documents/Estudos_Spark/spark-3.1.3-bin-hadoop3.2

Link para tutorial de instalação do Spark no Windowns:

https://www.youtube.com/watch?v=1gdOMSimjXk

Lembre-se de criar 3 variaveis de ambiente: SPARK_HOME, HADOOP_HOME E JAVA_HOME (sempre verifique se esse ultimo existe e está atualizado)