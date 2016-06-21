# Spark


## SparkContext ad sparkConf

任何spark程序的编写都是从SparkContext开始的。SparkContext需要初始化一个SparkConf对象，后者包含了Spark集群配置的各种参数。

初始化后，我们可以用SparkContext对象锁包含的各种方法来创建和操作分布式数据集和共享变量。

~~~scala
val conf = new SparkConf()
.setAppName("SomeName")
.setaster("local[4]")

val sc = new SparkContext(conf)
~~~

The code will create a SparkContext Object with 4 threads. The name of App is Somename. And then build a SparkContext object using the simple construction method with Spark

##Spark Shell
Spark支持用scala或者Python REPL(Read-Eval-Print-Loop)

## RDD
Resilient Distributed Dataset 是Spark的核心概念之一。一个RDD代表一个记录。

### 创建RDD
RDD可以从现有集合中创建：

```scala
val collection = List("a","b","c")
val rddFromCollection = sc.parallelize(collection)

```

也可以基于Hadoop的输入源创建，比如本地文件系统，HDFS和Amazon S3。基于Hadoop的RDD可以使用任何实现了Hadoop *InputFormat* 接口的输入格式，包括文本文件，其他


##Spark MLLib源码学习
### 位置：
spark-assembly-1.6.1-hadoopxxx.jar
org.apache.spark.mllib


