# ⚡ Apache Spark (PySpark)

O **Apache Spark** é o motor de processamento de dados distribuído líder de mercado. Ele foi projetado para processar volumes massivos de dados em clusters, utilizando computação em memória (In-Memory) para maximizar a performance.

## 🏗️ Arquitetura e Funcionamento
O Spark não armazena dados permanentemente; ele atua como uma camada de computação. Seus principais componentes são:
* **Driver Program:** O processo que executa o `main()` e cria o `SparkContext`.
* **Executors:** Processos nos nós do cluster que executam as tarefas de processamento e armazenam dados em cache.
* **Cluster Manager:** Gerencia os recursos (YARN, Mesos, Kubernetes ou Standalone).

## 🐍 Por que PySpark?
O PySpark é a API do Spark para Python. Ele permite que Engenheiros de Dados utilizem a sintaxe simples do Python enquanto aproveitam o poder do motor Scala/JVM do Spark por trás dos panos.

### Principais Vantagens:
1. **Velocidade:** Até 100x mais rápido que o Hadoop MapReduce em memória.
2. **Lazy Evaluation:** O Spark cria um plano de execução (DAG) e só processa os dados quando uma ação (como `.show()` ou `.write()`) é chamada.
3. **Versatilidade:** Suporta SQL, Streaming, Machine Learning (MLlib) e Processamento de Grafos.

---
